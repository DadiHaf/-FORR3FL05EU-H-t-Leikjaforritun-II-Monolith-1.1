# -FORR3FL05EU-H-t-Leikjaforritun-II-Monolith-1.1

28 Feb 2024
This is bit of a shallow update / explaination that I wanted to make because of the lackluster amount of material that I've turned in for the latest assignment (referring to the two screenshots).

The original idea of how the game's dialogue system was supposed to work was to ahve a class called StoryBlock would change the text of both the text on the dialogue screen and labels of choice boxes. It was supposed help it speed up the process of creating a conversation while also reducing the amount of 'if' statements needed in the code.

This is an example of what the class looked like.
class StoryBlock
{
    public string story; //dialogue screen text
    public string option1Text; //choice 1 text
    public string option2Text; //choice 2 text
    public StoryBlock option1Block;
    public StoryBlock option2Block;

    public StoryBlock(string story, string option1Text = "", string option2Text = "", StoryBlock option1Block = null, StoryBlock option2Block = null)
    {
        this.story = story;
        this.option1Text = option1Text;
        this.option2Text = option2Text;
        this.option1Block = option1Block;
        this.option2Block = option2Block;
    }
}

public class GameManager : MonoBehaviour
{
    static StoryBlock block1 = new StoryBlock("", "", "");
    static StoryBlock block2 =
...


I found it be a tedious process to manually insert texts into every new StoryBlock and so was trying to figure out how to update the button labels. I also had a hard time actually getting the code to work properly, which was not helped by the fact that I could't read the code properly for most of the time due to the naming bizarre convention that I chose to use.
One of the biggest problems with this class setup was that it only allowed two options at a time, which was a bit too limiting for what I was trying to accomplish.

I wasn't very happy about the state of the project at the time, so I tried looking up better options and I eventually found a Unity tutorial that used a program called Inkly which is specifically designed for creating interactive game narratives. I decided to ditch the original version of the game started a new project in Unity so I wouldn't have to rework the jumbled code that I've written. This happened quite late into development, so the actual game as it stands now is non-funtional and that's why I can only give two screenshots at the moment.

I'm planning on making an update some time soon that will go over the state of other aspects of the game.
