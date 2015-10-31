###One File MSBuild Project###

####Motivation####
I was building a few single file projects all having the same the include
folders, liibrary folders, the same libraries and the same destination folder.
It is rather painful to copy the vcxproj file, change the filename within this project and the project GUID. So I made the sample project file. Let me illustrate how to use it with an example. Say you have file DoSomthing.cpp and you want to create DoSomething.exe. You have to copy sample.vcxproj to DoSomething.vcxprojand then run this command in the MSbuild command line (console) window:

msbuild /t:Build  /p:Configuration=Release;Platform=x64 sample.vcxproj

Modify the vcxproj to local needs. 
If all you are doing is a one off application the Visual Studio IDE is better. But if you have to build many single file applications then you are better off using the command line and msbuild.



