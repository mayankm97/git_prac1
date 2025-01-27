<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Careers @ Oracle</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Google forms clone</h1>
    </header>
    <main>
        <h2>Job Application form</h2>
        <form action="#" method="get" novalidate  onsubmit="return customSubmitHandler()">
            <div class="form-group">
                <label for="name">Full Name:</label>
                <input type="text" id="name" name="name" placeholder="Enter your full name" required>
            </div>
            <div class="form-group">
                <label for="email">Email address:</label>
                <input type="email" id="email" name="email" placeholder="Enter your email" pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$" required>
            </div>
            
            <div class="form-group">
                <label for="phone">Phone Number:</label>
                <input type="tel" id="phone" name="phone" placeholder="Enter your phone number" 
                       pattern="^\+91\d{10}$" required>
            </div>
            
            <div class="form-group">
                <label for="password">Password:</label>
                <input type="password" id="password" name="password" placeholder="Enter your password" required>
            </div>
            <div class="form-group">
                <label for="dob">Date of Birth:</label>
                <input type="date" id="dob" name="dob" required>
            </div>
            <div class="form-group">
                <label for="position">Select the position you are applying for</label>
                <select id="position" name="position" required>
                    <option value="">Select a position</option>
                    <option value="sde">SDE</option>
                    <option value="designer">UI/UX designer</option>
                    <option value="manager">Product Manager</option>
                    <option value="Other">Other</option>
                </select>
            </div>

            <div class="form-group">
                <label>Skills:</label>
                <input type="checkbox" id="htm" name="skills" value="HTML">
                <label for="htm">HTML</label>
                <input type="checkbox" id="css" name="skills" value="CSS">
                <label for="css">CSS</label>
                <input type="checkbox" id="js" name="skills" value="JS">
                <label for="js">JavaScript</label>
                <input type="checkbox" id="mdb" name="skills" value="Mongo">
                <label for="mongo">MongoDB</label>            
            </div>

            <div class="form-group">
                <label>Availability</label>
                <input type="radio" id="full" name="availability" value="full">
                <label for="full">Full Time</label>
                <input type="radio" id="part" name="availability" value="part">
                <label for="part">Part Time</label>
                <input type="radio" id="office_intern" name="availability" value="office_intern">
                <label for="office_intern">Freelance</label>
            </div>

            <div class="form-group">
                <label for="time">Current time:</label>
                <input type="time" id="time" name="time" required>
            </div>

            <div class="form-group">
                <label for="resume">Upload Resume:</label>
                <input type="file" id="resume" name="resume" accept=".pdf,.doc,.docx">
            </div>
    
            <div class="form-group">
                <label for="cover-letter">Cover Letter:</label>
                <textarea id="cover-letter" name="cover-letter" rows="5" placeholder="Write a short cover letter..." maxlength="500"></textarea>
            </div>

            <div class="form-group">
                <label for="rating">Rate Your Skills (1-10):</label>
                <input type="range" id="rating" name="rating" min="1" max="10" step="1">
            </div>
    
            <div class="form-group">
                <label for="color">Pick Your Favorite Color:</label>
                <input type="color" id="color" name="color" value="#6200ea">
            </div>
    
            <input type="hidden" name="form_id" value="job-application-form">
    
            <button type="submit">Submit Application</button>
        </form>
        
        <script>
            function customSubmitHandler() {
                alert('Form submitted!');
                return false;
            }
        </script>
    </main>
</body>
</html>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Arial', sans-serif;
    background-color: #f4f7f6;
    color: #333;
    padding: 20px;
}

main {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

h2 {
    text-align: center;
    color: #4A90E2;
    margin-bottom: 20px;
}

.form-group {
    margin-bottom: 15px;
}

label {
    font-weight: bold;
    color: #4A90E2;
    margin-bottom: 5px;
    display: inline-block;
}

input[type="text"],
input[type="email"],
input[type="tel"],
input[type="password"],
input[type="date"],
input[type="time"],
input[type="file"],
textarea,
select {
    width: 100%;
    padding: 10px;
    margin: 5px 0 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 14px;
}

input[type="checkbox"],
input[type="radio"] {
    margin-right: 5px;
    margin-left: 0;
    vertical-align: middle;
}

input[type="file"] {
    padding: 10px 0;
}

textarea {
    resize: vertical;
}

form {
    padding: 20px;
    background-color: #f9f9f9;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

form .form-group {
    margin-bottom: 20px;
}

form button[type="submit"] {
    width: 100%;
    padding: 12px;
    background-color: #4A90E2;
    color: white;
    border: none;
    border-radius: 4px;
    font-size: 16px;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

form button[type="submit"]:hover {
    background-color: #357ABD;
}

.checkbox-group, .radio-group {
    display: flex;
    gap: 5px;
    align-items: center;
    flex-wrap: wrap;
}

.checkbox-group label, .radio-group label {
    margin-left: 5px;
}

.form-group input[type="checkbox"]:not(:last-child),
.form-group input[type="radio"]:not(:last-child) {
    margin-right: 8px;
}

.form-group label {
    margin-right: 8px;
}
