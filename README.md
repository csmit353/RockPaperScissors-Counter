# RockPaperScissors-Counter
let Weapon = 0
input.onGesture(Gesture.Shake, function () {
    Weapon = Math.randomRange(1, 3)
    if (Weapon == 1) {
        basic.showLeds(`
            # # # # #
            # . . . #
            # . . . #
            # . . . #
            # # # # #
            `)
    } else if (Weapon == 2) {
        basic.showLeds(`
            . . . . .
            . # # # .
            . # # # .
            . # # # .
            . . . . .
            `)
        basic.showLeds(`
            . . . . .
            . . . . .
            . # # # .
            # # # # .
            . # # # #
            `)
        basic.showLeds(`
            . . . . .
            # . . . .
            . # # # #
            . # # # .
            . # # # .
            `)
        basic.showLeds(`
            # . . . #
            . . . . .
            . # # # .
            . # # # .
            . # # # .
            `)
    } else {
        basic.showLeds(`
            # # . . #
            # # . # .
            . . # . .
            # # . # .
            # # . . #
            `)
        basic.showLeds(`
            . . . . .
            # # . . .
            # # # # #
            # # . . .
            . . . . .
            `)
        basic.showLeds(`
            # # . . #
            # # . # .
            . . # . .
            # # . # .
            # # . . #
            `)
    }
})
input.onButtonPressed(Button.A, function () {
    game.addScore(1)
    basic.pause(100)
    basic.showString("Wins:")
    basic.showNumber(game.score())
})
