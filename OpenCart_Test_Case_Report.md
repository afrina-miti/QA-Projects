Test Case Report – OpenCart Demo

Summary Statistics:

Total Test Cases: 68
✅ Pass: 57
❌ Fail: 9
⚠️ N/A: 2
🔐 Login & Authentication
Test Case ID Title Steps Expected Result Actual Result Status
TC_01 Valid Login 1. Go to login page 2. Enter valid email & password 3. Click Login User logged in successfully User logged in successfully ✅ Pass
TC_02 Invalid Password 1. Enter correct email 2. Enter wrong password 3. Click Login Error message shown Error message shown ✅ Pass
TC_03 Empty Fields 1. Leave email & password empty 2. Click Login Validation message shown Validation message shown ✅ Pass
TC_04 Invalid Email Format 1. Enter invalid email (abc) 2. Enter password 3. Click Login Validation error for email format Validation error for email format ✅ Pass
TC_05 Unregistered Email 1. Enter unregistered email 2. Enter any password 3. Click Login Error: account not found Error message shown ✅ Pass
TC_06 Password Case Sensitivity 1. Enter correct email 2. Enter password in wrong case 3. Click Login Login should fail Login failed ✅ Pass
TC_07 Remember Me Function 1. Check 'Remember Me' 2. Login 3. Close and reopen browser User remains logged in Remember Me option not available on login page ⚠️ Fail / N/A
TC_08 Logout Functionality 1. Login 2. Click 'My Account' 3. Click Logout User logged out; redirected to home User logged out successfully ✅ Pass
TC_09 Forgot Password – Valid Email 1. Click 'Forgotten Password' 2. Enter registered email 3. Submit Password reset email sent Password reset email sent successfully ✅ Pass
TC_10 Forgot Password – Unregistered Email 1. Click 'Forgotten Password' 2. Enter unregistered email 3. Submit Error: email not found Error message shown ✅ Pass
TC_11 Login After Logout 1. Login 2. Logout 3. Login again with same credentials User logged in successfully User logged in successfully ✅ Pass
TC_12 Session Timeout 1. Login 2. Stay inactive for long period 3. Try to perform action Session expires; redirect to login User remains logged in without re-authentication ❌ Fail
📝 Registration
Test Case ID Title Steps Expected Result Actual Result Status
TC_13 Valid Registration 1. Go to Register page 2. Enter all valid details 3. Agree to Privacy Policy 4. Click Continue Account created successfully Account created successfully ✅ Pass
TC_14 Missing Required Fields 1. Leave required fields empty 2. Click Continue Validation errors shown Validation errors shown ✅ Pass
TC_15 Invalid Email Format 1. Enter invalid email 2. Fill other fields 3. Submit Email validation error Email validation error shown ✅ Pass
TC_16 Password Mismatch 1. Enter password 2. Enter different confirm password 3. Submit Error: passwords do not match Confirm Password field not available ⚠️ Fail / N/A
TC_17 Duplicate Email Registration 1. Register with already-registered email 2. Submit Error: email already exists Error message displayed ✅ Pass
TC_18 Weak Password Acceptance 1. Enter 1-character password 2. Fill other fields 3. Submit System should reject weak password System accepts weak password without validation ❌ Fail
TC_19 Privacy Policy Checkbox 1. Fill all fields 2. Do NOT check Privacy Policy 3. Submit Validation: must agree to Privacy Policy Validation message shown ✅ Pass
TC_20 Special Characters in Name Field 1. Enter name with special chars (!@#) 2. Fill other fields 3. Submit Validation error for invalid name System accepts special characters in name ❌ Fail
🔍 Search
Test Case ID Title Steps Expected Result Actual Result Status
TC_21 Valid Product Search 1. Enter 'iPhone' in search bar 2. Click Search Relevant products displayed Relevant products displayed ✅ Pass
TC_22 Invalid Product Search 1. Enter 'xyz999abc' 2. Click Search 'No results' message shown No results message shown ✅ Pass
TC_23 Empty Search 1. Leave search box empty 2. Click Search System handles empty search gracefully System handled empty search properly ✅ Pass
TC_24 Partial Keyword Search 1. Enter partial word 'mac' 2. Click Search Matching products displayed Matching products displayed ✅ Pass
TC_25 Search with Special Characters 1. Enter '@#$%' 2. Click Search System handles without crashing System handled input properly ✅ Pass
TC_26 Very Long Input in Search 1. Enter 200+ character text 2. Click Search System handles input properly System handled input properly ✅ Pass
TC_27 Case-Insensitive Search 1. Enter 'IPHONE' 2. Click Search Results same as lowercase search Results displayed correctly ✅ Pass
TC_28 Search Result Click 1. Search for 'mac' 2. Click on a product from results Product detail page opens Product detail page opened correctly ✅ Pass
🛍️ Product & Product Detail
Test Case ID Title Steps Expected Result Actual Result Status
TC_29 Product Detail Page Load 1. Click on any product from listing Product detail page loads with name, price, image, description Product detail page loaded successfully ✅ Pass
TC_30 Product Image Display 1. Open product detail page Product image should display clearly Product image displayed ✅ Pass
TC_31 Add to Wishlist 1. Open product page 2. Click 'Add to Wish List' Product added to wishlist Requires login – redirected to login page ✅ Pass
TC_32 Product Compare 1. Select 2 products 2. Click Compare Comparison table shown Comparison page displayed ✅ Pass
TC_33 Product Review – Valid 1. Open product page 2. Scroll to Reviews 3. Enter name, review, rating 4. Submit Review submitted successfully Review submitted – pending approval message shown ✅ Pass
TC_34 Product Review – Empty Fields 1. Open review form 2. Leave all fields empty 3. Submit Validation errors shown Validation errors shown ✅ Pass
TC_35 Out-of-Stock Product Add to Cart 1. Find unavailable product 2. Click 'Add to Cart' Proper out-of-stock message shown Product added to cart despite being unavailable ❌ Fail
TC_36 Product Price Display 1. Open any product page Price should display correctly with currency Price displayed correctly ✅ Pass
🛒 Shopping Cart
Test Case ID Title Steps Expected Result Actual Result Status
TC_37 Add Product to Cart 1. Select a product 2. Click 'Add to Cart' Product added successfully Product added successfully ✅ Pass
TC_38 Add Multiple Products 1. Add different products to cart All products appear in cart All products appeared in cart ✅ Pass
TC_39 Increase Quantity 1. Add product 2. Increase quantity 3. Click Update Quantity updates correctly Quantity updated correctly ✅ Pass
TC_40 Decrease Quantity to Zero 1. Add product 2. Set quantity to 0 3. Click Update Product removed or validation shown Product removed from cart ✅ Pass
TC_41 Remove Product from Cart 1. Add product 2. Click Remove (X) Product removed from cart Product removed successfully ✅ Pass
TC_42 Cart Persistence After Login 1. Add items to cart 2. Login 3. Check cart Cart items retained after login Cart items retained ✅ Pass
TC_43 View Cart Page 1. Add product 2. Click cart icon Cart page opens with product details Cart page displayed correctly ✅ Pass
TC_44 Empty Cart Message 1. Open cart with no items Message: 'Your shopping cart is empty!' Empty cart message shown ✅ Pass
💳 Checkout
Test Case ID Title Steps Expected Result Actual Result Status
TC_45 Checkout with Valid Details 1. Add product 2. Proceed to checkout 3. Enter valid details 4. Confirm order Order placed successfully Unable to place order – stock error message shown ❌ Fail
TC_46 Checkout without Login 1. Add product 2. Go to checkout without logging in System should ask to login/register Shopping cart appears empty; cannot proceed ❌ Fail
TC_47 Empty Checkout Fields 1. Go to checkout 2. Leave required fields empty 3. Continue Validation errors shown Stock availability message shown instead of validation ❌ Fail
TC_48 Invalid Payment Details 1. Enter invalid payment info 2. Confirm order Payment error message shown Stock availability message shown ❌ Fail
TC_49 Apply Coupon – Valid 1. Add product 2. Enter valid coupon 3. Apply Discount applied successfully Discount applied ✅ Pass
TC_50 Apply Coupon – Invalid 1. Add product 2. Enter invalid coupon 3. Apply Error: invalid coupon Error message shown ✅ Pass
TC_51 Order Confirmation Page 1. Complete checkout successfully Order confirmation page with order ID Cannot reach confirmation page due to checkout bug ❌ Fail
TC_52 Checkout Address Autofill 1. Login 2. Proceed to checkout Saved address autofills in billing section Saved address autofilled correctly ✅ Pass
👤 My Account
Test Case ID Title Steps Expected Result Actual Result Status
TC_53 View Account Dashboard 1. Login 2. Go to My Account Account dashboard displays correctly Dashboard displayed correctly ✅ Pass
TC_54 Edit Account Information 1. Login 2. My Account → Edit Account 3. Change name 4. Save Account info updated successfully Account info updated successfully ✅ Pass
TC_55 Change Password – Valid 1. Login 2. Change Password 3. Enter current & new password 4. Save Password changed successfully Password changed successfully ✅ Pass
TC_56 Change Password – Wrong Current 1. Login 2. Change Password 3. Enter wrong current password Error: incorrect current password Error message shown ✅ Pass
TC_57 View Order History 1. Login 2. My Account → Order History All past orders listed Order history displayed ✅ Pass
TC_58 View Order Detail 1. Login 2. Order History 3. Click on an order Order details displayed Order details page displayed correctly ✅ Pass
TC_59 Manage Address Book – Add 1. Login 2. Address Book → Add New Address 3. Fill details 4. Save New address saved successfully New address saved successfully ✅ Pass
TC_60 Manage Wishlist 1. Login 2. Add product to wishlist 3. View wishlist Wishlist shows added product Wishlist displayed with product ✅ Pass
🏠 Homepage & Navigation
Test Case ID Title Steps Expected Result Actual Result Status
TC_61 Homepage Load 1. Open https://demo.opencart.com/
Homepage loads with banner, featured products, navbar Homepage loaded successfully ✅ Pass
TC_62 Navigation Menu – Categories 1. Hover over category in nav menu Dropdown shows subcategories Dropdown displayed correctly ✅ Pass
TC_63 Featured Products Display 1. Open homepage Featured products visible with images and prices Featured products displayed ✅ Pass
TC_64 Footer Links 1. Scroll to footer 2. Click on any link (e.g., About Us) Correct page opens Correct page opened ✅ Pass
TC_65 Contact Us Page 1. Click Contact Us 2. Fill form 3. Submit Message sent confirmation shown Confirmation message shown ✅ Pass
TC_66 Currency Change 1. Click currency dropdown 2. Select different currency Prices update to selected currency Prices updated correctly ✅ Pass
TC_67 Responsive Layout – Mobile View 1. Open site on mobile or resize browser Site should be responsive and usable Site displayed responsively ✅ Pass
TC_68 Page Load Speed 1. Open homepage Page should load within 3 seconds Page loaded within acceptable time
