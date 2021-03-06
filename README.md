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
#### Assignment 2
Ok this one was fun, you can find the solution [here](https://github.com/ATahhan/CardShuffle/tree/assignment-2). Something worth mentioning is that I don't think this is the best solution, there might be better ways to achieve the goal or I might be even totally wrong. Please take it for just what it is and nothing more.

## Lecture 5

Following on the same project: [CardShuffle](https://github.com/ATahhan/CardShuffle), in this lecture we had a chance to refactor some of the old code, and learn more about and apply @ViewBuilder wrapper, as well as the ViewModifier protocol. Check [lecture-5](https://github.com/ATahhan/CardShuffle/tree/lecture-5) branch.

## Lecture 6

Last lecture working on the project [CardShuffle](https://github.com/ATahhan/CardShuffle). We've looked at the animations in SwiftUI and how they can be derived by the app state itself. Unfortunately the way animations are presented in the course isn't the best IMHO, here are a couple more resources to help you better understand this subject (in case you feel lost like I did):
- Most important resource on SwiftUI animations is the [interactive toturial](https://developer.apple.com/tutorials/swiftui/animating-views-and-transitions) by Apple itself. Really amazing resource to get introduced into the subject.
- [Animation Juice in SwiftUI](https://www.dotconferences.com/2020/02/pavel-zak-animation-juice-in-swiftui) by [Pavel Zak](https://twitter.com/myridiphis) also gives a great introduction and explains important concepts around the SwiftUI animations not covered by the course.
- A worth mentioning tutorial is this [article](https://www.answertopia.com/swiftui/swiftui-animation-and-transitions/) I've used some of the code samples provided, really amazing
- [This one](https://www.dotconferences.com/2020/02/tobias-due-munk-prototyping-custom-ui-in-swiftui) isn't about SwiftUI animations exactly, but it's showing its great potential and is very, very fun to watch.
