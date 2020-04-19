# Suckmore Shell 2.0


> After its abysmal performance at WPICTF 2019, suckmore shell v1 has been replaced with a more secure, innovative and performant version, aptly named suckmore shell V2.

> ssh smsh@smsh.wpictf.xyz pass: suckmore>suckless

> made by: acurless


When we ssh to the account, we arrive to a custom shell. By using ls, we see a single flag called flag, probably what we're looking for.

The password is actually a hint to tell us to use "more" and not "less" or "cat".
Indeed, if we do

	less flag
	
or

	cat flag

We just get a black loading screen and nothing is printed.

	more flag
	
On the other end print us the following text: 
> echo "WPI{SUckmoreSoftwareN33dz2G3TitTogeTHER}"

**flag**: WPI{SUckmoreSoftwareN33dz2G3TitTogeTHER}