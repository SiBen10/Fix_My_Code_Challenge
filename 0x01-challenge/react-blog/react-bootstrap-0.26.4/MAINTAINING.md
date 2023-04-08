# Maintaining React-Bootstrap

This document is for people working on React-Bootstrap. It describes common tasks such as triaging or merging pull requests.

If you are interested in contributing to React-Bootstrap, you should check out the Contributing Guide.

# Triaging Issues

New issues pop up every day. We need to identify urgent issues (such as nobody can use a component, or install React-Bootstrap), close and link duplicates, answer questions, etc. Please alert the gitter/react-bootstrap chat room of the urgent issues. We are using HuBoard which is a kanban style board to track and prioritize issues.

Some issues are opened that are just too vague to do anything about. If after attempting to get feedback from issue authors fails after 7 days, then close the issue. Please inform the issue author that they may re-open if they are able to present the requested information.

# Merging a pull request

Please, make sure:

Travis build is green
At least one collaborator (other than you) approves the PR
Commenting "LGTM" (Looks good to me) or something of similar sorts is sufficient.
If it's a simple docs change or a typo fix, feel free to skip this step.
Commits follow the convention prescribed in the Contributing Guide.
This is very important, because the release process uses this to generate the changelog.
Commits are squashed. Each change is a single commit.
e.g. if the PR contains two changes such as [fixed] Some Bug and then [fixed] Some other unrelated bug it should be two separate changes.
e.g. if the first commit is [fixed] Some bug and the second commit is [fixed] failing tests for previous commit, you should squash them into a single commit
It's alright to ask the author of the pull request to fix any of the above.

# Becoming a maintainer

If you are interested in becoming a react-bootstrap maintainer, start by reviewing issues and pull requests. Answer questions for those in need of troubleshooting. Join us in the gitter/react-bootstrap chat room. Once we see you helping, either we will reach out and ask you if you want to join or you can ask one of the organization owners to add you. We will try our best to be proactive in reaching out to those that are already helping out.

GitHub by default does not publicly state that you are a member of the organization. Please feel free to change that setting for yourself so others will know who's helping out. That can be configured on the organization list page.

Being a maintainer is not an obligation. You can help when you have time and be less active when you don't. If you get a new job and get busy, that's alright.

# Releases

Releases should include documentation, git tag, bower package preparation and finally the actual npm module publish. We have all of this automated by running npm run release. PLEASE DO NOT RUN npm publish BY ITSELF. The release-script will do that. We want to prevent issues like #325 and #218 from ever happening again. In order to run the release-script you will need permission to publish the package to npm. Those with this permission are in the publishers team

Note: The publishers team does exist. If you see 404 that means you just have no permissions to publish.

Example usages of the release-script:
