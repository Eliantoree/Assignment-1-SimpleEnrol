# Assignment-1-SimpleEnroll
Assignment 1: SimpleEnroll

Download  Link :https://programming.engineering/product/assignment-1-simpleenroll/

Description
5/5 – (2 votes)
It’s that time of the quarter again; time to use SimpleEnroll again Wootwoot.

One thing everyone realizes in their Stanford career at one point is that they have to eventually graduate — and so enrolling in classes becomes a strategic endeavor to maximize the XP towards graduation, while also being able to sleep more than 4 hours a night!

In this hopefully short assignment, we’re going to use data from the ExploreCourses API to fgure out which CS classes on ExploreCourses are ofered this year, and which are not! We’ll be taking advantage of streams, while also exercising initialization and references in C++. Lets jump in ʕ•́ᴥ•̀ʔっ

There are really only two fles you should care about:

utils.cpp

Main.cpp

Please do the following to download the starter code here! Please unzip the fle.

Spoiler, you

Part 0: Read the code + add paths + Course struct

Take a look at the main.cpp function, and take special notice of how vector_of_courses is passed into parse_csv, write_courses_offered, and write_courses_not_offered. Think about what these functions are

doing, do you need to change anything in the function defnition?

do.

In the main.cpp and utils.cpp you need to manually add paths to the code. Here’s how you can do this.

In VSCode:

Paste the path of

courses_ofered.csv as a string in the variable std::string

COURSES_OFFERED_CSV_PATH

courses_not_offered.csv as a string in the variable std::string

COURSES_NOT_OFFERED_CSV_PATH

Write the correct types for the felds in the Course struct. Remember what types streams deal with?

Part 1: parse_csv

Check out courses.csv, it is a csv fle, with three columns: Title, Number of Units, and Quarter. Implement parse_csv so that, for each line in the csv fle, it creates a struct Course containing the Title, Number of Units, and Quarter for that line.

A couple of things you need to think about:

1) How are you going to read in courses.csv? Muahahaha, perhaps a stream ?

2) How will you get each line in the fle?

Hints:

Make use of the split function we provide to get a vector that looks like the following: [Title, Number of Units, Quarter]

Check out the implementation – ask us any questions about it – you should be able to reason about it since it’s using a stringstream

Part 2: write_courses_offered

Ok. Now you have a populated vector_of_courses which has all of the records of the courses.csv fle neatly stored in a Course struct! You fnd yourself interested in only the courses that are ofered, right? In this function, write out to student_output/courses_offered.csv all the courses that don’t have “null” or the quarter feld.

IMPORTANT → When writing out to the fle please follow this format:

<Title>,<Number of Units>,<Quarter>

There are no spaces between the commas! The autograder will not be happy if this format is not followed!

Additionally, keep track of the classes that are ofered perhaps with another vector and delete them from vector_of_courses. This means that after this function runs, vector_of_courses should ONLY contain classes that are not ofered! For this, be sure to take a look at the PROVIDED function: delete_elem_from_vector!

Don’t worry, I know you’re wondering what this is:

auto it = std::find(v.begin(), v.end(), elem);

We got you……in like 3 weeks.

Part 3: write_courses_not_offered

So you’re curious about classes that aren’t ofered…curiosity hurt the cat. In the

write_courses_not_offered function, write out to

student_output/courses_offered.csv the classes in vector_of_courses.

Remember since you deleted the classes that are ofered in part 2,

vector_of_courses trivially contains ONLY classes that are not ofered – lucky

you. So this step should look really similar to part 2 except shorter and a tiny bit

simpler

Congrats you’re done!

The instructions to submit this assignment will be posted on Ed closer to the assignment deadline

Plz leave feedback here!


Shoutout

A special thank you to Jim Sproch for providing the ExploreCourses API. After an unsuccessful attempt to web-scrape the ExploreCourses website, I was directed to Jim Sproch who was kind enough to not only provide us the API but also answer our questions about its use!

