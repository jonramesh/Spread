<!--
This file provides context/instruction for your repository! They are written in Markdown (.md), for simple formatting:
https://www.markdownguide.org/cheat-sheet/
-->

# Project 2: *Spread*

Demo/template for our [second projects](https://typography-interaction-2627.github.io/project/2/).

> **Students will now work together—with a new reading from those selected by the class in [*Manuscript*](https://typography-interaction-2627.github.io/project/1/)—to express a text deliberately and consistently across devices.**
>
> The goal of this project is twofold: both an effective *collaboration* between partners and also a successful, *responsive* design. Each duo will sketch cooperatively and then implement a joint execution together, via pair programming. The final web page will be responsive for mobile, desktop, and print layouts.


# Why we chose this Design
> Throughout the readings, the authors discuss branding, graphic design, and real-world brand logos while showing examples of grid templates, images, and white space. Inspired by these visual concepts, we decided to frame our website around a "Grid + Branding" concept.
>To reflect this, we used solid and dashed lines to visually expose the grid system of the layout. For the branding element, we created radio buttons that allowed users to change the entire website's color palette to match the specific brand colors featured in the article.
>We specifically chose red and sky blue as the primary colors for our website to serve both a structural and a branding purpose. Red represents the sharp, structural precision of the grid lines, while sky blue provides a cool, dynamic background that emphasizes the white space and imagery. Together, this bold contrast establishes a strong brand identity before the user interacts with the radio buttons to switch to other brand palettes featured in the reading.





# Type system



`
   /* make it browser defaut 16px, make it a percentage( look into it ) */
    font-size: 125%;
    --size-h1: clamp(1rem, 3vw, 3rem);
    --size-h1-xl: clamp(2rem, 15vw, 17rem);
    --size-h2:1.5rem;
    --size-p:1rem;
    --color-background:#BAE8FF;
    --color-text:#FF0001;
    --leading: 2cap;
    --size-logo:1rem;
    line-height: var(--leading);

	 /* vertical spacing using root line height to preserve vertical ryhthm */
	--space-block-xs:.25rlh;
	--space-block-s:.5rlh;
	--space-block-m:1rlh;
	--space-block-l:2rlh;


	 /*Horizontal spacing using rem to preserve Horizontal consistency */

	--space-inline-xs:.5rem;
	--space-inline-s:.75rem;
	--space-inline-m:1rem;
	--space-inline-l:1.5rem;
	--space-inline-xl:2rem;

	 /*Fonts */

	 --font-bugrino:'Bugrino', sans-serif;
	 --font-sans-serif:'Arial', sans-serif;
`

>In this code we used a 125% for the root font size becuase of the default font-size of most browsers being 16px we wanted out to be 20px.we used this base for all out spacing though the rem ad rlh property. rem is used for both the font-size to create a consistent relationship between all sizes. This is transferedto the inline sizing so all horiatal spacing cotiues the relationship. Than we used rlh becuase we wanted to taking the base line height and use that for all out vertical spacing so that we a vertical rythm amoungst all our elements.



# Heading Container
________

>Its contained in the bigger article grid no matter if its in mobile,tablet,desktop it will be on the top. It used the height 40vh on mobile to keep the proportions of the text and we increase it slightly to 60vh and 70vh so that it can become a bigger hero moment in desktop

## Grid Typography
_____

>So it uses an 8 column grid with 4 column rows. This is because no matter what in mobile or desktop the rows do not change. We use an 8 columns grid so that the fonts can always be space relationally to the olli dos  no matter how you expand from Mobile to Desktop. It uses a h1 as the base with a bigger h1 that is in its separate class that emphasizes the Ollie Dos and Donts

# The Identifier
______

>Its place in the article grid using the grid-area with the name info. We use flex to organize and have it stack vertically

## Author and time Section
______
>It uses border top and bottom to keep with the grided motif.We use flex to first space it so that no matter how big the screen is they will always be evenly spaced between each other.Flex-direction row is used so that it is spaced horizontally, we wrote it so you can understand the direction .



# Nav
_______

>Its a sticky navigation on top for the table of contents. Used a flex box and centered it
> We then used a link and targeted it to the position of each heading within the article

## Details
_______

>The box surrounded for the table of contents

## Summary
______
>The text that contains the "Table of Contents"

# Article
______
> we decieded to use a grid and its functio template areas to create a modular layout that allowed us to do a stacked layout for mobile while changing it to a split view in Desktop/Tablet

# Quote
____

`
#quote{
	padding-block:var(--space-block-l);
	flex-direction:column; /*--vertical--*/

		>:first-child{
			font-family: 'Bugrino',sans-serif;
			font-weight: 500;
			font-size: 1rem;
			font-style: italic;
			border-block-start: 1px solid var(--color-text);
			border-block-end: 1px dashed var(--color-text);
			border-inline: 1px solid var(--color-text);
			padding: var(--space-inline-xl);
			margin-block:0rem;
		}
		>:nth-child(2){
			font-family: 'Bugrino',sans-serif;
			font-weight: 500;
			font-size: 1rem;
			font-style: italic;
			border-block-end: 1px dashed var(--color-text);
			border-inline: 1px solid var(--color-text);

			padding: var(--space-inline-xl);
			margin-block:0rem;
		}
		>:nth-child(3){

			font-family: 'Bugrino',sans-serif;
			font-weight: 500;
			font-size: 1rem;
			font-style: italic;
			border-block-end: 1px dashed var(--color-text);
			border-inline: 1px solid var(--color-text);
			padding: var(--space-inline-xl);
			margin-block:0rem;
		}
		>:nth-child(4){
			font-family: Arial, Helvetica, sans-serif;
			font-weight: 100;
			text-align: center;
			border-block-end: 1px solid var(--color-text);
			border-inline: 1px solid var(--color-text);
			padding: var(--space-inline-m);
			margin-block:0rem;
			}

		}

`
> We decided to use fle direction column to stack all the quote paragraphs together. We used the dashed line to keep the consistency fo the motif throughout the webiste. Its not three diferent quotes but split up and spaced by the dashed lines




# Branding Buttons

>our sources we used for it
>Source for radio buttons: https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/input/radio
>Source for has:
>https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Selectors/:has
>Inspiration for the background changing effects:
>https://github.com/cheny511-pixel/manuscript


> a grid which holds the stylized radio buttons it changes from a 2 column grid to a 1 column grid

`
input[type ="radio"]{

			border-radius:100%;
			width:.75rem;
			height:.75rem;
			border: 2px solid var(--color-text);



		}
		input:checked {
  		border: 6px solid var(--color-text);
			}


`

> custom styles for the input buttons for the radio. We customized both the checked state and the default state




# Snoopy-Text-Image

`

#snoopy-image{

    font-family:'Bugrino',sans-serif;
    display:flex;
    flex-wrap:wrap;
    --box-side:10rem;
    gap:3cap;

    >span{
        border: 1px solid var(--color-text);
        width:var(--box-side);
        height:var(--box-side);
        font-size:1.25rem;
        align-self:end;

        /* adding some sketches */

        display:grid;
        grid-template-columns: 1fr 4fr 1fr;
        grid-template-rows: 1fr 2fr 7fr 2fr 1fr;

        >.vertical-column-1{
            grid-column:1;
            grid-row:1/span 5;
            border-inline-end:1px dashed var(--color-text);

        }
        >.vertical-column-2{
            grid-column:2;
            grid-row:1/span 5 ;
            border-inline-end:1px dashed var(--color-text);

        }
        >.vertical-column-3{
            grid-column:3;
            grid-row:1/span 5;


        }
        >.horizantal-row-1{
            grid-column:1/span 3;
            grid-row:2;
            border-block:1px dashed var(--color-text);


        }
        >.horizantal-row-2{
            grid-column:1/span 3;
            grid-row:4;
            border-block:1px dashed var(--color-text);
        }
        :nth-child(6){

            grid-column:2;
            grid-row:3;



        }




    }


}
`
>We used span as containers because we felt that sematically it was more decoration so  it did not have any really semantic significance.

>Each span uses grid and overlapping child spans to recreate the logo grid for each word. Each span contains the dotted border which allows us to recreate that grid within our work

>The grid allows us to have overlapping elements which allows us to recreate this motif. We use grid span to put all the spans in its proper space while allowing us to contain the text in the middle.


# text-image
_____
`
#text-image{

    display:grid;
    grid-template-columns: auto auto;
    grid-template-rows:auto auto;




`

>Gird auto template allows us to have the grid snap to the size of the inner contents.

`
>.word-hierarchy{

		display:flex;
		flex-direction:column; /*--vertical--*/
		font-family: 'Bugrino',sans-serif;




		>:first-child{
			margin-bottom: var(--space-block-m);
		}

		>:nth-child(2){
			font-size: 1.25rem;
			margin-bottom: var(--space-block-m);
		}

		>:nth-child(3){
			font-size: 1.5rem;
			margin-bottom: var(--space-block-m);
		}

		>:nth-child(4){
			font-size: 1.75rem;
			margin-bottom: var(--space-block-m);
		}


	}
	/* targets the first and second word-heriarchy so we do ot have to repeat code ad put them both in different grid-columns*/
	>:first-child{
			grid-column:1;

	}
	>:nth-child(2){
			grid-column:2;

	}


	/*--the text with two-lined box--*/
	>#big-moment{


		grid-column:1/span 2;

		border:1px solid var(--color-text);
		padding: var(--space-inline-l);


		>:first-child{
			font-size: 2rem;
			font-family:'Bugrino';
			font-weight: 800;
			padding-inline: var(--space-inline-l);
			border:1px solid var(--color-text);

			@media(width > 800px){

				font-size:4rem;





			}
		}
# What I learned

>Throughout the process, I learned more about communication and responsibility. Because there were only two of us and we had to do it together, every line of code I wrote and every design decision I made directly impacted my partner’s workflow. Knowing that my work was the foundation for theirs motivated me to be more thorough and meet our deadlines consistently. For the codes, trying to have a responsive website made me basically learn a lot about the grid systems and flex box.

> I learned alot about compromise and accomedating someone elses schedule so the dynemic is not alays on oly one persons time. We also came from differet skill levels but we ended up being able to teach other alot of things and be open to feedback from your partner allows both of you to grow as you complete this project. I can remember the large amont of small mistakes I made that would have eaten up alot of time but having someone else there to review and correct those mistakes makes things more efficent. Overall this was a realy great leanring experience as I was both had to understad and be able to expain those conepts to someone else,instead of leaving them in my own headspace.

`

> since world heirarchy styles are the exact same we decided
