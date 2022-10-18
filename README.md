<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div style="justify-content: center; margin-left: 50%;">
        <h2>Michael Y</h2>
        <img style="text-align: center;" src="https://www.w3schools.com/images/w3schools_green.jpg" alt="W3Schools.com">
        <div>
            <button style="text-align: center;" onclick="showSkills()">Show Skill</button>
        </div>
        <div id="skillList">
        </div>

        <div id="comments">
            <p>Comments:</p>
        </div>

        <input type="text" id="commentInput">
        <button onclick="addComments()">Add</button>
    </div>

    <script>
        const skills = ["JavaScript", "Angular", "Java", "Spring Boot"];
        function showSkills(){
            let del = document.getElementById("skills");
            if(del)
                del.remove();
            

            let skill = document.getElementById("skillList");
            let list = document.createElement("ul");
            list.setAttribute("id", "skills")

            skills.forEach((skill)=>{
                let row = document.createElement("li");
                let skillTxt = document.createTextNode(skill);
                row.appendChild(skillTxt);
                list.appendChild(row);
            })

            skill.appendChild(list);
        }

        function addComments(){
            let comment = document.getElementById("commentInput").value;

            let commentList = document.getElementById("comments");
            let list = document.createElement("ul");
            list.setAttribute("id", "cmts")

            let row = document.createElement("li");
            let commentTxt = document.createTextNode(comment);
            row.appendChild(commentTxt);
            list.appendChild(row);

            commentList.appendChild(list);
        }
    </script>
</body>
</html>
