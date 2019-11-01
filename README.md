# imgMARK
image watermarking tool - Hackathon build. Developer Camp 2019

This is a hackathon built project that lays the groundwork for an image watermarking tool. The tool encrypts a hidden watermark in photos
by "punching out" a hole in the photo and layering the punched out watermark behind the image. This ensures that anyone attempting to display
a stolen image will have a portion of the photo missing.

This code can be run by completing the following steps in terminal:
npm install

npm run serve

to view the application navigate to http://localhost:8080/
The "case study" page demonstrates a mock shutterstock site with images using the imgMARK watermark. Drag these images off of the page to see
the punched out watermark.

The frontend of this code sample uses the VueJS framework. This was used due to time constraints during the 24 hour hackathon, as Vue has a quick setup time.
