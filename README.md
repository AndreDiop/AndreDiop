### Hi there 👋<br/>
I'm Andre Diop, a Full Stack web developer from Atlanta. My passion for web development lies with the creation of ideas and making them come true with user intuitive interfaces. I take great care in the experience, architecture, and code quality of the things I build.  

🌱 I’m currently learning more about Java, Cloudformation, CI/CD and AWS Deployments  
👯 I’m looking to collaborate on projects no matter how big or small.  


[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FAndreDiop&count_bg=%23B6ED9A&title_bg=%235DD3C9&icon=&icon_color=%23E7E7E7&title=Visits&edge_flat=true)](https://hits.seeyoufarm.com)







<!--
**AndreDiop/AndreDiop** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on an application that allows users to 
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
- 📫 How to reach me:
-->


a!localVariables(
  local!showPopup: false,
  {
    a!sectionLayout(
      showWhen: not(local!showPopup),
      contents: {
        a!textField(
          label: "Text",
        ),
        a!paragraphField(
          label: "Paragraph",
        ),
        a!buttonArrayLayout(
          buttons: {
            a!buttonWidget(
              label: "Show Popup!",
              icon: "arrow-right",
              value: true,
              saveInto: local!showPopup,
              style: "PRIMARY"
            )
          },
          align: "CENTER"
        )
      },
    ),
    a!columnsLayout(
      showWhen: local!showPopup,
      columns: {
        a!columnLayout(),
        a!columnLayout(
          contents: {
            a!cardLayout(
              marginAbove: "EVEN_MORE",
              showBorder: false,
              showShadow: true,
              contents: {
                a!sectionLayout(
                  contents: {
                    a!richTextDisplayField(
                      labelPosition: "COLLAPSED",
                      value: {
                        a!richTextItem(
                          text: {
                            "This is a fake popup window!"
                          },
                          size: "MEDIUM_PLUS"
                        ),
                        char(10),
                        char(10),
                        "And shows some text to the user."
                      }
                    )
                  },
                  divider: "BELOW"
                ),
                a!buttonLayout(
                  primaryButtons: {
                    a!buttonWidget(
                      label: "OK",
                      icon: "check",
                      style: "PRIMARY",
                      value: false,
                      saveInto: local!showPopup
                    )
                  },
                  secondaryButtons: {
                    a!buttonWidget(
                      label: "Cancel",
                      icon: "times",
                      style: "NORMAL",
                      value: false,
                      saveInto: local!showPopup
                    )
                  }
                )
              },
            )
          }
        ),
        a!columnLayout()
      },
    )
  }
)
