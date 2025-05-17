1.Creating the Jenkins Job

Opened Jenkins and clicked on “New Item”. Created a Freestyle project and named it Newitem. Under the Source Code Management section, selected Git. Entered my GitHub repository URL: [https://github.com/sneha-182003/Jenkins-tas](https://github.com/Sanjana-np/Jenkins-Job-Creation_Implementing-Version-Control-in-Your-CI-CD-Pipeline) Changed the branch specification from master to main, since my GitHub repo uses main as the default branch.

Adding Build Steps
In the Build section, I added a Windows batch command. I used the following command to simulate a simple build: echo "Building the project..." This command was added in the “Execute Windows batch command” section and used to verify that Jenkins executes the build step after cloning the repository.

Running the Build and Output
Clicked Build Now to trigger the build manually. Viewed the logs under Console Output, which showed the following:

![WhatsApp Image 2025-05-17 at 18 54 56_b7e1bdc9](https://github.com/user-attachments/assets/c8ed7f76-e73d-459f-a2bc-2e68bcb1c982)

This confirmed that Jenkins successfully: Fetched the code from GitHub Checked out the correct commit Executed the batch command Finished the build successfully

Challenges Faced and Solution

I initially got an error: “Couldn't find any revision to build.” This happened because Jenkins was looking for the master branch, which didn’t exist in my GitHub repo. I resolved it by changing the branch specifier in Jenkins to main.

![Uploading WhatsApp Image 2025-05-17 at 18.54.56_4437d96d.jpg…]()

