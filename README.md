# Get More Ram
A simple [StosSign](https://github.com/stossy11/StosSign) wrapper app that allows you to enable "Increased Memory Limit" for your sideloaded apps without using Xcode.

It fixes an error -80045 and -22411 by changing client/user-agent to
" <Windows;6.2(0,0);9200> <com.apple.AuthKit/1 (com.apple.iTunes/12.12.4.1)>

akd/1.0 CFNetwork/808.1.4"

It fixes this error but then people were getting an error -22411. As it was descibed in altsign repo
"Since October 13 Apple often pushes the verification code to trusted
devices right after the password step. In that case the complete
response has hsc 409 and no "au" value, so we used to skip 2FA, ask for
app tokens right away and fail with -22411 (This action cannot be
completed at this time)."

So to fix this I with the help of AI ported their solution into GetMoreRam by implementing AltSign fix into StosSign’s Authentication.swift.

# How to use
1. Sideload this app
2. Go to settings, sign in your account that you used to sign the app you want to enable "Increased Memory Limit"
3. Go to "App IDs" page
4. Tap Refresh
5. Tap the app you want to enable "Increased Memory Limit"
6. Tap "Add Increased Memory Limit"
7. Reinstall the app from SideStore/AltStore
8. Check if you have "Increased Memory Limit"

# Credits
Stossy11 - For StosSign.
SideStore - Anisette Data fetching codes are stolen from SideStore
