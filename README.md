
Balloontip component
--------------------

Plugin page: [http://artifacts.griffon-framework.org/plugin/balloontip](http://artifacts.griffon-framework.org/plugin/balloontip)


Provides a balloontip component. Based on [Balloontip][1].

Usage
-----

The following nodes will become available on a View script upon installing this plugin

| Node                 | Property         | Type                      | Default                | Required | Bindable | Notes                                                             |
| -------------------- | ---------------- | ------------------------- | ---------------------- | -------- | -------- | ----------------------------------------------------------------- |
| balloontip           | text             | String                    |                        | yes      | no      | can be set as the node's value if `component:` is present         |
|                      | component        | JComponent                |                        | yes      | no       | can be set as the node's value if `text:` is present              |
|                      | style            | BalloonStyle              |                        | no       | yes      |                                                                   |
|                      | alignment        | BalloonTip.Orientation    | BalloonTip.Orientation | no       | no       |                                                                   |
|                      | attachLocation   | BalloonTip.AttachLocation | ALIGNED                | no       | no       |                                                                   |
|                      | horizontalOffset | int                       | 16                     | no       | no       |                                                                   |
|                      | verticalOffset   | int                       | 20                     | no       | no       |                                                                   |
|                      | useCloseButton   | boolean                   | true                   | no       | no       |                                                                   |
|                      |                  |                           |                        |          |          | accepts nested BallonStyles                                       |
| customBalloonTip     | text             | String                    |                        | yes      | no       | can be set as the node's value if `component:` is present         |
|                      | component        | JComponent                |                        | yes      | no       | can be set as the node's value if `text:` is present              |
|                      | offset           | Rectangle                 |                        | yes      | no       | may also be a List of 4 ints                                      |
|                      | style            | BalloonStyle              |                        | no       | yes      |                                                                   |
|                      | alignment        | BalloonTip.Orientation    | BalloonTip.Orientation | no       | no       |                                                                   |
|                      | attachLocation   | BalloonTip.AttachLocation | ALIGNED                | no       | no       |                                                                   |
|                      | horizontalOffset | int                       | 16                     | no       | no       |                                                                   |
|                      | verticalOffset   | int                       | 20                     | no       | no       |                                                                   |
|                      | useCloseButton   | boolean                   | true                   | no       | no       |                                                                   |
|                      |                  |                           |                        |          |          | accepts nested BallonStyles                                       |
| tablecellBalloonTip  | text             | String                    |                        | yes      | no       | can be set as the node's value if `component:` is present         |
|                      | component        | JComponent                |                        | yes      | no       | can be set as the node's value if `text:` is present              |
|                      | row              | int                       |                        | yes      | no       |                                                                   |
|                      | column           | int                       |                        | yes      | no       |                                                                   |
|                      | style            | BalloonStyle              |                        | no       | yes      |                                                                   |
|                      | positioner       | BalloonTipPositioner      |                        | no       | yes      |                                                                   |
|                      | alignment        | BalloonTip.Orientation    | BalloonTip.Orientation | no       | no       |                                                                   |
|                      | attachLocation   | BalloonTip.AttachLocation | ALIGNED                | no       | no       |                                                                   |
|                      | horizontalOffset | int                       | 16                     | no       | no       |                                                                   |
|                      | verticalOffset   | int                       | 20                     | no       | no       |                                                                   |
|                      | useCloseButton   | boolean                   | true                   | no       | no       |                                                                   |
|                      |                  |                           |                        |          |          | accepts nested BallonStyles                                       |
| edgedBalloonStyle    | fillColor        | Color                     | Color.WHITE            | no       | no       |                                                                   |
|                      | borderColor      | Color                     | Color.BLACK            | no       | no       |                                                                   |
| minimalBalloonStyle  | fillColor        | Color                     | Color.WHITE            | no       | no       |                                                                   |
|                      | arcWidth         | int                       | 5                      | no       | no       |                                                                   |
| modernBalloonStyle   | topColor         | Color                     | Color.WHITE            | no       | no       |                                                                   |
|                      | bottomColor      | Color                     | Color.LIGHT_GRAY       | no       | no       |                                                                   |
|                      | borderColor      | Color                     | Color.BLACK            | no       | no       |                                                                   |
|                      | arcWidth         | int                       | 5                      | no       | no       |                                                                   |
|                      | arcHeight        | int                       | 5                      | no       | no       |                                                                   |
| roundedBalloonStyle  | fillColor        | Color                     | Color.WHITE            | no       | no       |                                                                   |
|                      | borderColor      | Color                     | Color.BLACK            | no       | no       |                                                                   |
|                      | arcWidth         | int                       | 5                      | no       | no       |                                                                   |
|                      | arcHeight        | int                       | 5                      | no       | no       |                                                                   |
| texturedBalloonStyle | image            | Image                     |                        | yes      | no       |                                                                   |
|                      | url              | URL                       |                        | yes      | no       |                                                                   |
|                      | file             | File                      |                        | yes      | no       | may also be a `String`                                            |
|                      | inputStream      | InputStream               |                        | yes      | no       |                                                                   |
|                      | resource         | String                    |                        | yes      | no       |                                                                   |
|                      | class            | Class                     |                        | yes      | no       | only required if `resource` is specified.                         |
|                      | borderColor      | Color                     | Color.BLACK            | no       | no       |                                                                   |
|                      | arcWidth         | int                       | 5                      | no       | no       |                                                                   |
|                      | arcHeight        | int                       | 5                      | no       | no       |                                                                   |
|                      |                  |                           |                        |          |          | specify one of `image`, `url`, `file`, `inputStream`, `resource`. |

The [Balloontip manual] explains with greta detail how these components can be used.

### Example

Here are some examples of the `balloontip` nodes in action

        package sample

        application(title: 'Balloontip',
          preferredSize: [320, 240],
          pack: true,
          locationByPlatform:true,
          iconImage: imageIcon('/griffon-icon-48x48.png').image,
          iconImages: [imageIcon('/griffon-icon-48x48.png').image,
                       imageIcon('/griffon-icon-32x32.png').image,
                       imageIcon('/griffon-icon-16x16.png').image]) {
            vbox {
                label("Move your mouse over the buttons")
                button("Hides on mouse exit", id: "b2",
                    mouseEntered:{ bt2.visible = true },
                    mouseExited:{ bt2.visible = false })
                button("Hides after 5s", id: "b1",
                    mouseEntered:{ bt1.visible = true })
                button("Regular balloontip", id: "b3",
                    mouseEntered:{ bt3.visible = true })
                button("Balloontip with Modern style", id: "b4",
                    mouseEntered:{ bt4.visible = true },
                    mouseExited:{ bt4.visible = false })

                balloonTip(b1, id: "bt1",
                    text: "I'll hide myself in 5s",
                    hideAfter: 5000,
                    useCloseButton: false)
                balloonTip(b2, id: "bt2",
                    text: "Hover outside my anchor and I'll hide",
                    useCloseButton: false)
                balloonTip(b3, id: "bt3",
                    text: "Click close and will never show up again",
                    useCloseButton: true)
                balloonTip(b4, id: "bt4",
                    text: "Modern style applied",
                    useCloseButton: false) {
                    modernBalloonStyle(
                        topColor: java.awt.Color.WHITE,
                        bottomColor: java.awt.Color.RED,
                        arcWidth: 8,
                        arcHeight: 8
                    )
                }
            }
        }


[1]: http://balloontip.java.net
[2]: http://balloontip.java.net/manual.html

