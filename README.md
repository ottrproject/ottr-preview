# ottr-preview

This action can create previews of your Rmd, Quarto, or markdown websites on an open pull requests. 

It will create a report and comment on your open pull request if put in a workflow that uses the `pull_request` trigger. 

<img width="765" alt="Screenshot 2025-04-04 at 11 26 11 AM" src="https://github.com/user-attachments/assets/809dd069-270e-4615-ab03-96959b37ab73" />

## How to use: 

You can make a preview like this for an Rmd/Quarto website or course. 
```
steps:
    - name: Checkout Actions Repository
      uses: actions/checkout@v4
      with:
        fetch-depth: 0

    - name: Run render for Rmd
      uses: ottrproject/ottr-preview@cansavvy-patch-1
      with:
        toggle_website: "rmd"
```

## Parameters 

- `toggle_website` - can be "rmd", "rmd_web", "quarto", or "quarto_web" for bookdown render, markdown render, or quarto render. 
- `root_path` is how you can specify where the base of your website is (will look for files like "index.Rmd"). Default is current working directory. 

