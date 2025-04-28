# csc4140-assignment-2-solved
**TO GET THIS SOLUTION VISIT:** [CSC4140 Assignment 2 Solved](https://www.ankitcodinghub.com/product/csc4140-assignment-ii-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;116879&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSC4140 Assignment 2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
1 From Model to Screen

If we want to get a model to screen, we bacially need the following steps:

1. Model Translation T

2. Model Scaling S

3. Model Rotation R

4. View Translation

5. View Rotation

6. Project

Written in Matrix production:

ModelV iewProject = Project · V iewR · V iewT · ModelS · ModelR · ModelT (1)

For this assignment, your tasks are

1.1 Implement Model Matrix (40 Points)

Complete the given function.

get_model_matrix(float rotation_angle,

Eigen::Vector3f T,

Eigen::Vector3f S,

Eigen::Vector3f P0,

Eigen::Vector3f P1):

1

2

3

4

5

Note: express the tranforms in each steps use homogeneous coordinates. For example use 4×

Matrix to express the translation Vector3f T. (You can also validate your results by using the

Eigen’s lib function.)

Follow the instructions in the give code structure.

1.2 Implement perspective projection Matrix (40 Points)

get_projection_matrix(float eye_fov,

float aspect_ratio, float zNear, float Zfar)

1

2

3

4

1.3 Implement main() function according to your needs (20 Points)

int main(int argc, const char** argv)

{

\your code

}

1

2

3

4

1.4 Useful information you need this time

\Member Variables

\three transformation matrix

Matrix4f model, view, projection;

\frame buffer: cache what you want to draw on screen vector&lt;Vector3f&gt; frame_buf;

\Member Functions

\transfer model matrix as \parameters to rasterizer(given) set_model(const Eigen::Matrix4f&amp; m)

\set view transformation to view matrix set_view(const Eigen::Matrix4f&amp; v)

\ transfer projection matrix to rasterizer set_projection(const Eigen::Matrix4f&amp; p)

\ set pixel(i ,j) on screen with color (r,g,b)

1

2

3

4

5

6

7

8

9 10

11

12

13

14

15

16

17

18

19

\ and write to frame buffer set_pixel(Vector2f point, Vector3f color)

20

21

2 Your report (20 Points)

For this assignment, 10% is for the template using. Do submit your report using the given template in the first assignment. 80% is listed in Section 1. 10% is for your completing you main() function and make it easier to use (e.g., define a .xml file to record eye_position, rotation angle or other parameters. This part is not limited)

In your report,

1) You need to define a proper eye position freely

2) define a proper triangle

3) define your eye_fov, aspect_ratio, zNear, zFar.

4) all other missing information

You need to think where you should define the object (triangle), your eye position and other parameters. As if you cannot define a proper parameters, you might get nothing on your screen as your “eye” cannot see it. So in your report, write down this parameters by either inside your code or an extra parameter file (e.g. .xml which you do not always need compile the code), and show the corresponding results on the screen.

In your report, I would like to see at least two corresponding results (at least see a triangle on your screen, you can put more). Make it easier to run for TAs, just save the results images as “results_1.png, results_2.png, …). Your report and your code result must match each other.

submission list all naming roles is given in last assignment, zip them together submit it.

1) PDF report

2) codes

3) CMake file

4) Readme: describe how to run your code and some extra work you think I can give you more

grades.

5) a bash file that can compile the code, run the code(save the results). Direct run and see result.
