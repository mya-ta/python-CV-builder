# CV Builder using python (Mini project)

## Installation
Run `python install -r requirements.txt`

![cv](https://github.com/user-attachments/assets/22613f96-a3b1-4fb2-9bf6-898168730fbf)

# Handle the variations (using a loop for multiple variations)
            for i in range(int(request.POST.get('num_variations', 0))):  # 'num_variations' is passed from the form
                variation_form = ProductVariationForm(request.POST, request.FILES)
                variation_forms.append(variation_form)
                if variation_form.is_valid():
                    variation = variation_form.save(commit=False)
                    variation.product = product  # Assign the product to the variation
                    variation.save()
