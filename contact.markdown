---
layout: default
title: Contact
permalink: /contact/
---

<div style="display: flex; flex-direction: column; justify-content: flex-start; align-items: flex-start; height: 80vh; padding-top: 10vh; padding-right: 6.25%;">
    <span style="font-size: 1.2em;">Thank you for taking the time to view my work.</span>
    <span style="font-size: 1.2em; margin-top: 1em;">If you'd like to contact me, please use the form below:</span>
    <div style="border: 2px solid #000; padding: 20px; width: 40%; background-color: #FFFFFF; color: black; margin-top: 1em; border-radius: 10px; box-sizing: border-box;">
        <div style="display: flex; justify-content: flex-start; margin-top: 20px;">
            <form id="contact-form" action="https://formspree.io/f/xblgrbpw" method="POST" style="font-size: 1.2em; width: 100%;">
                <label for="email"><strong>Your Email:</strong></label><br>
                <input type="email" id="email" name="email" required style="background-color: white; color: black; border: 2px solid #000; border-radius: 5px; width: 100%;"><br><br>
                
                <label for="subject"><strong>Subject:</strong></label><br>
                <input type="text" id="subject" name="subject" required style="background-color: white; color: black; border: 2px solid #000; border-radius: 5px; width: 100%;"><br><br>
                
                <label for="message"><strong>Message:</strong></label><br>
                <textarea id="message" name="message" rows="4" required style="background-color: white; color: black; border: 2px solid #000; border-radius: 5px; width: 100%;"></textarea><br><br>
                
                <input type="submit" value="Send" style="border-radius: 5px;">
            </form>
        </div>

        <p id="form-response" style="text-align: left; margin-top: 15px; font-size: 1.2em; color: green;"></p>

        <p style="text-align: left; margin-top: 25px; font-size: 1.2em;"><em>Or you can reach out directly at: <a href="mailto:gabocreates@gmail.com"><u>gabocreates@gmail.com</u></a></em></p>
    </div>
</div>

<script>
document.getElementById("contact-form").addEventListener("submit", async function(event) {
    event.preventDefault(); // Prevent default form submission
    const form = event.target;
    const formData = new FormData(form);

    try {
        const response = await fetch(form.action, {
            method: "POST",
            body: formData,
            headers: { "Accept": "application/json" }
        });

        if (response.ok) {
            document.getElementById("form-response").innerText = "Thank you! Your message has been sent.";
            form.reset();
        } else {
            document.getElementById("form-response").innerText = "Oops! There was an error submitting the form.";
        }
    } catch (error) {
        document.getElementById("form-response").innerText = "Something went wrong. Please try again.";
    }
});
</script>
