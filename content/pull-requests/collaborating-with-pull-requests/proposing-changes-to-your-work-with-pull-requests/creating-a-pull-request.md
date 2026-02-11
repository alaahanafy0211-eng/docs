---
العنوان: إنشاء طلب سحب
مقدمة: "إنشاء طلب سحب لاقتراح التغييرات في مستودع والتعاون بشأنها. وتقترح هذه التغييرات في... *فرع.*مما يضمن أن الفرع الافتراضي يحتوي فقط على عمل مكتمل ومعتمد. "
الأذونات: "يمكن لأي شخص لديه حق الوصول إلى مستودع إنشاء طلب سحب.{% data reusables.enterprise-accounts.emu-permission-propose%}"
redirect_من:
  -           /Github/التعاون مع القضايا والسحب الطلبات/اقتراح التغييرات في عملك مع طلبات السحب/إنشاء طلب سحب.         
  -           /المقالات/إنشاء-طلب سحب.         
  -             /Github/التعاون مع القضايا وطلبات السحب/إنشاء طلب سحب.           
الإصدارات:
 FPT: " ghes: "*"*'
 ghes: '*'
 ghes: ' *
المواضيع:
  -          سحب الطلبات.        
---

    إذا كنت ترغب في إنشاء فرع جديد لطلب السحب الخاص بك وليس لديك أذونات الكتابة إلى المستودع، يمكنك شوكة المستودع أولاً. لمزيد من المعلومات، انظر.      [العنوان الذاتي.]   (/سحب الطلبات / التعاون مع طلبات السحب / اقتراح التغييرات في عملك مع طلبات السحب / إنشاء طلب سحب من شوكة.) و...     [العنوان الذاتي.](/سحب-طلبات/التعاون مع-سحب-طلبات/العمل مع الشوك/حول الشوك.).

يمكنك تحديد الفرع الذي ترغب في دمج التغييرات فيه عند إنشاء طلب السحب. لا يمكن فتح طلبات السحب إلا بين فرعين مختلفين.

{% البيانات reusables.pull_requests.perms-to-open-pull-request%}

العنوان: إنشاء طلب سحب

##        تغيير نطاق الفروع ومستودع الوجهة.      

   بشكل افتراضي، تستند طلبات السحب إلى الفرع الافتراضي للمستودع الأم. لمزيد من المعلومات، انظر.     [العنوان الذاتي.](/سحب-طلبات/التعاون مع-سحب-طلبات/اقتراح-التغييرات-لعملك-مع-سحب-طلبات/حول-فروع#حول-الفرع الافتراضي-الفرع).

إذا لم يكن مستودع الوالدين الافتراضي صحيحًا، فيمكنك تغيير كل من المستودع الأم والفرع باستخدام القوائم المنسدلة. يمكنك أيضًا تبديل رأسك وفروعك الأساسية بالقوائم المنسدلة لإنشاء خلافات بين النقاط المرجعية. يجب أن تكون المراجع هنا أسماء فروع في مستودع GitHub الخاص بك.

     /Github/التعاون مع القضايا وطلبات السحب/إنشاء طلب سحب.   

  العنوان: إنشاء طلب سحب_base branch_ is    **أين؟**   يجب تطبيق التغييرات، و   _رئيس الفرع._   يحتوي على...   **ماذا؟!**   كنت ترغب في أن تطبق. 

---

العنوان: إنشاء طلب سحب

يمكنك تحديد الفرع الذي ترغب في دمج التغييرات فيه عند إنشاء طلب السحب. لا يمكن فتح طلبات السحب إلا بين فرعين مختلفين.[!TIP]
(/سحب-طلبات/التعاون مع-سحب-طلبات/العمل مع الشوك/حول الشوك.). * Using the compare view, you can set up comparisons across any timeframe. For more information, see [AUTOTITLE](/pull-requests/committing-changes-to-your-project/viewing-and-comparing-commits/comparing-commits).
> * Project maintainers can add a pull request template for a repository. Templates include prompts for information in the body of a pull request. For more information, see [Autotitle.](/communities/using-templates-to-encourage-useful-issues-and-pull-requests/about-issue-and-pull-request-templates).

## Creating the pull request

(/سحب-طلبات/التعاون مع-سحب-طلبات/اقتراح-التغييرات-لعملك-مع-سحب-طلبات/حول-فروع#حول-الفرع الافتراضي-الفرع).

(/سحب-طلبات/التعاون مع-سحب-طلبات/اقتراح-التغييرات-لعملك-مع-سحب-طلبات/حول-فروع#حول-الفرع الافتراضي-الفرع).
1. In the "Branch" menu, choose the branch that contains your commits.

   ![Screenshot of the branch dropdown menu on the main page of a repository.](/assets/images/help/pull_requests/branch-dropdown.png)

{% data reusables.repositories.new-pull-request %}
1. Use the _base_ branch dropdown menu to select the branch you'd like to merge your changes into, then use the _compare_ branch drop-down menu to choose the topic branch you made your changes in.
{% data reusables.repositories.pr-title-description %}
{% data reusables.repositories.create-pull-request %}

{% data reusables.repositories.asking-for-review %}

After your pull request has been reviewed, it can be [merged into the repository](/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/merging-a-pull-request).

{% endwebui %}

{% cli %}

{% data reusables.cli.cli-learn-more %}

To create a pull request, use the `gh pr create` subcommand.

```shell
gh pr create
```

To assign a pull request to an individual, use the `--assignee` or `-a` flags. You can use `@me` to self-assign the pull request.

```shell
gh pr create --assignee "@octocat"
```

To specify the branch into which you want the pull request merged, use the `--base` or `-B` flags. To specify the branch that contains commits for your pull request, use the `--head` or `-H` flags.

```shell
gh pr create --base my-base-branch --head my-changed-branch
```

To include a title and body for the new pull request, use the `--title` and `--body` flags.

```shell
gh pr create --title "The bug is fixed" --body "Everything works again"
```

To mark a pull request as a draft, use the `--draft` flag.

```shell
gh pr create --draft
```

To add a labels or milestones to the new pull request, use the `--label` and `--milestone` flags.

```shell
gh pr create --label "bug,help wanted" --milestone octocat-milestone
```

To add the new pull request to a specific project, use the `--project` flag.

```shell
gh pr create --project octocat-project
```

To assign an individual or team as reviewers, use the `--reviewer` flag.

```shell
gh pr create --reviewer monalisa,hubot --reviewer myorg/team-name
```

To create the pull request in your default web browser, use the `--web` flag.

```shell
gh pr create --web
```

{% endcli %}

{% desktop %}

1. Click **Preview Pull Request**. {% data variables.product.prodname_desktop %} will open a preview dialog showing the diff of the changes between your current branch and the base branch.

   {% mac %}

   ![Screenshot of the "No local changes" view. A button, labeled "Preview Pull Request", is highlighted with an orange outline.](/assets/images/help/desktop/mac-preview-pull-request.png)

   {% endmac %}

   {% windows %}

   ![Screenshot of the "No local changes" view. A button, labeled "Preview Pull Request", is highlighted with an orange outline.](/assets/images/help/desktop/windows-preview-pull-request.png)

   {% endwindows %}

   Alternatively, to go straight to {% data variables.product.prodname_dotcom %} to create your pull request, select the dropdown icon and click **Create Pull Request**.

1. Confirm that the branch in the **base:** dropdown menu is the branch where you want to merge your changes.

   ![Screenshot of the "Open a Pull Request" dialog window. A button with a dropdown icon, labeled "base: development", is outlined in orange.](/assets/images/help/desktop/base-branch-selection.png)

   {% data variables.product.prodname_desktop %} will advise you whether the current branch can be automatically merged into the base branch.

   ![Screenshot of the "Open a Pull Request" dialog window. A status label stating "Can't automatically merge" is highlighted with an orange outline.](/assets/images/help/desktop/preview-dialog-merge-status.png)

1. Click **Create Pull Request**. {% data variables.product.prodname_desktop %} will open your default browser to take you to {% data variables.product.prodname_dotcom %}.
{% data reusables.repositories.pr-title-description %}
{% data reusables.repositories.create-pull-request %}

{% enddesktop %}

{% ifversion fpt or ghec %}

{% codespaces %}

1. Once you've committed changes to your local copy of the repository, click the **Create Pull Request** icon.
![Screenshot of the top of the "Source Control" side bar. The pull request icon is highlighted with a dark orange outline.](/assets/images/help/codespaces/codespaces-commit-pr-button.png)
1. Check that the local branch and repository you're merging from, and the remote branch and repository you're merging into, are correct. Then give the pull request a title and a description.
![Screenshot of the "{% data variables.product.prodname_dotcom %} Pull Request" side bar with a form for creating a pull request, including "Title" and "Description" fields.](/assets/images/help/codespaces/codespaces-commit-pr.png)
1. Click **Create**.

For more information on creating pull requests in {% data variables.product.prodname_github_codespaces %}, see [AUTOTITLE](/codespaces/developing-in-codespaces/using-github-codespaces-for-pull-requests).

{% endcodespaces %}

{% endif %}

## Making changes to files in your pull request

After you have opened your pull request, you can continue making changes to the files by adding new commits to your head branch.

{% webui %}

You can also make changes to files on the {% data variables.product.github %} website.

1. On {% data variables.product.github %}, navigate to a pull request in a repository.
{% data reusables.repositories.changed-files %}
1. Scroll down to the file you want to make changes to.
   * If the pull request has a lot of files, you can use the filter to locate the file. See [AUTOTITLE](/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/filtering-files-in-a-pull-request).
1. Above the file you want to change, click {% octicon "kebab-horizontal" aria-label="Show options" %}.
   ![Screenshot of the options above a file on the "File changed" tab. The "Show options" button is highlighted with an orange rectangle.](/assets/images/help/pull_requests/menu-on-pull-request-file.png)
1. In the menu, click **Edit file**.
1. Make your changes in the editor and when committing your change, choose to commit directly back to your head branch.

{% endwebui %}

## Further reading

* [AUTOTITLE](/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork)
* [AUTOTITLE](/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/keeping-your-pull-request-in-sync-with-the-base-branch)
* [AUTOTITLE](/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/changing-the-base-branch-of-a-pull-request){% ifversion projects-v1 %}
* [AUTOTITLE](/issues/organizing-your-work-with-project-boards/tracking-work-with-project-boards/adding-issues-and-pull-requests-to-a-project-board#adding-issues-and-pull-requests-to-a-project-board-from-the-sidebar){% endif %}
* [AUTOTITLE](/issues/tracking-your-work-with-issues/creating-an-issue)
* [AUTOTITLE](/issues/tracking-your-work-with-issues/assigning-issues-and-pull-requests-to-other-github-users)
* [AUTOTITLE](/get-started/writing-on-github)
