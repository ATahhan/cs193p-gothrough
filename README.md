# CS193p Go-Through

Find below the details and assignments/projects. Updated regularly upon progressing. Course page can be found [here](https://cs193p.sites.stanford.edu/)

## Lecture 1 & 2

This is the [CardShuffle](https://github.com/ATahhan/CardShuffle) project repo with its assignments .

## Lecture 3

Following on the same project: [CardShuffle](https://github.com/ATahhan/CardShuffle), this lecture showed how to implement Combine for more reactive UI, with some changes and a bit of code refactoring. (check [lecture-3](https://github.com/ATahhan/CardShuffle/tree/lecture-3) branch).

## Lecture 4

A couple notes I'd like to add on this lecture's code [CardShuffle](https://github.com/ATahhan/CardShuffle):

```swift
struct MemoryGame<CardContent> where CardContent: StringProtocol {
```
Here I've used `StringProtocol` on `CardContent` generic type because that's what the current views know how to draw as a content. This should be a more generic protocol where adopters specify how content is drawn rather than what is its identity.

Also, I'm not using the custom `Array` extensions used in the lectures because I didn't feel like repeating what the native `firstIndex(where:)` function already do just for the convenience of passing it a card object instead of comparing ids.

I liked how the `Grid` is designed, keeps preferred aspect ratio with the ability to have a row with less than max count. Another way to do grids can be found [here](https://www.hackingwithswift.com/quick-start/swiftui/how-to-position-views-in-a-grid).