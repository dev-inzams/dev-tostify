    Create HTML File:
        Open your preferred code editor.
        Create a new HTML file (e.g., index.html).
        Copy and paste the HTML code provided in the previous response into your HTML file.

    Create CSS File:
        Create a new CSS file (e.g., styles.css).
        Copy and paste the CSS code provided in the previous response into your CSS file.

    Create JavaScript File:
        Create a new JavaScript file (e.g., script.js).
        Copy and paste the JavaScript code provided in the previous response into your JavaScript file.

    Open in Browser:
        Save all your files.
        Open the HTML file (index.html) in your web browser.

    Test Toasts:
        Click the "Show Success Toast" button to see a success toast notification.
        Click the "Show Error Toast" button to see an error toast notification.

    Customize:
        You can customize the toast appearance and behavior by modifying the CSS in the styles.css file.
        Feel free to change the toast messages or add more buttons as needed.

Remember that this example is a basic implementation of toast notifications using HTML, CSS, and JavaScript. It provides a starting point that you can expand and customize based on your specific requirements.

if you to want to use in laravel you can use this
	async function updateCategory() {
        try{
            let updatecategory = document.getElementById('updatecategory').value
            let category_id = document.getElementById('updatecategory').dataset.id
            let res = await axios.post("/update-category",{'category_id' : category_id,'name' : updatecategory});
            if(res.data['status'] == 'success'){
                closeModal();
                successToast(res.data['message']); 
                await getCategories();
            }
        }catch(error){
            errorToast('Something went wrong')
        }
    }