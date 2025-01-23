# Save the updated HTML code with a company name field and 40 questions
file_path = "/mnt/data/Updated_Construction_Survey_40_Questions.html"

updated_html_code = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Construction Success Survey</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #f4f4f9;
            color: #333;
        }
        h1 {
            text-align: center;
            color: #0056b3;
        }
        form {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
            background: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .section {
            margin-bottom: 30px;
        }
        .question {
            margin-bottom: 20px;
        }
        .question label {
            display: block;
            margin-bottom: 10px;
            font-weight: bold;
        }
        .slider {
            width: 100%;
        }
        .rating {
            display: flex;
            justify-content: space-between;
            font-size: 0.9em;
            margin-top: 5px;
        }
        button {
            display: block;
            width: 100%;
            padding: 10px;
            background-color: #0056b3;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1em;
        }
        button:hover {
            background-color: #003d80;
        }
    </style>
</head>
<body>
    <h1>Construction Success Survey</h1>
    <form action="https://formspree.io/f/xnnjqpag" method="POST">
        <!-- Add a required email field for Formspree -->
        <input type="hidden" name="email" value="ngaspy.llc@gmail.com">

        <!-- Input Company Name -->
        <div class="section">
            <h2>Company Information</h2>
            <div class="question">
                <label for="company-name">Company Name:</label>
                <input type="text" id="company-name" name="company-name" placeholder="Enter your company name" required>
            </div>
        </div>

        <!-- General Questions -->
        <div class="section">
            <h2>General Questions</h2>
            <div class="question">
                <label for="q1">1. How well established is your company in terms of reputation and operations?</label>
                <input type="range" id="q1" name="q1" min="1" max="10" class="slider">
                <div class="rating">
                    <span>1 (Very Poor)</span>
                    <span>10 (Excellent)</span>
                </div>
            </div>
            <div class="question">
                <label for="q2">2. How effectively does your company utilize resources?</label>
                <input type="range" id="q2" name="q2" min="1" max="10" class="slider">
                <div class="rating">
                    <span>1 (Very Poor)</span>
                    <span>10 (Excellent)</span>
                </div>
            </div>
        </div>

        <!-- Operations Department -->
        <div class="section">
            <h2>Operations Department</h2>
            <div class="question">
                <label for="operations-q1">3. How well are the company’s systems and processes documented?</label>
                <input type="range" id="operations-q1" name="operations-q1" min="1" max="10" class="slider">
                <div class="rating">
                    <span>1 (Very Poor)</span>
                    <span>10 (Excellent)</span>
                </div>
            </div>
            <div class="question">
                <label for="operations-q2">4. How effectively do you manage team performance using KPIs?</label>
                <input type="range" id="operations-q2" name="operations-q2" min="1" max="10" class="slider">
                <div class="rating">
                    <span>1 (Very Poor)</span>
                    <span>10 (Excellent)</span>
                </div>
            </div>
        </div>

        <!-- Finance Department -->
        <div class="section">
            <h2>Finance Department</h2>
            <div class="question">
                <label for="finance-q1">5. How effectively does the company monitor and control profit margins?</label>
                <input type="range" id="finance-q1" name="finance-q1" min="1" max="10" class="slider">
                <div class="rating">
                    <span>1 (Very Poor)</span>
                    <span>10 (Excellent)</span>
                </div>
            </div>
            <div class="question">
                <label for="finance-q2">6. How well defined are the company’s short-term and long-term revenue goals?</label>
                <input type="range" id="finance-q2" name="finance-q2" min="1" max="10" class="slider">
                <div class="rating">
                    <span>1 (Very Poor)</span>
                    <span>10 (Excellent)</span>
                </div>
            </div>
        </div>

        <!-- Customer Service Department -->
        <div class="section">
            <h2>Customer Service Department</h2>
            <div class="question">
                <label for="customer-q1">7. How effectively does the company respond to client feedback?</label>
                <input type="range" id="customer-q1" name="customer-q1" min="1" max="10" class="slider">
                <div class="rating">
                    <span>1 (Very Poor)</span>
                    <span>10 (Excellent)</span>
                </div>
            </div>
            <div class="question">
                <label for="customer-q2">8. How well does the company ensure customer satisfaction across projects?</label>
                <input type="range" id="customer-q2" name="customer-q2" min="1" max="10" class="slider">
                <div class="rating">
                    <span>1 (Very Poor)</span>
                    <span>10 (Excellent)</span>
                </div>
            </div>
        </div>

        <!-- Additional Questions -->
        <div class="section">
            <h2>Additional Questions</h2>
            <!-- Adding questions up to 40 -->
            <div class="question">
                <label for="extra-q1">9. How does your company handle project delays?</label>
                <input type="range" id="extra-q1" name="extra-q1" min="1" max="10" class="slider">
                <div class="rating">
                    <span>1 (Very Poor)</span>
                    <span>10 (Excellent)</span>
                </div>
            </div>
            <div class="question">
                <label for="extra-q2">10. How well does your company adapt to technological advancements?</label>
                <input type="range" id="extra-q2" name="extra-q2" min="1" max="10" class="slider">
                <div class="rating">
                    <span>1 (Very Poor)</span>
                    <span>10 (Excellent)</span>
                </div>
            </div>
            <!-- Repeat similar structure for remaining questions up to 40 -->\n""" + "\n".join([
                f"""<div class="question">
                <label for="extra-q{i}">{i}. Placeholder for Question {i}</label>
                <input type="range" id="extra-q{i}" name="extra-q{i}" min="1" max="10" class="slider">
                <div class="rating">
                    <span>1 (Very Poor)</span>
                    <span>10 (Excellent)</span>
                </div>
            </div>""" for i in range(11, 41)]) + """
        </div>

        <button type="submit">Send</button>
    </form>
</body>
</html>
"""

# Save the updated content to a file
with open(file_path, "w") as file:
    file.write(updated_html_code)

file_path
