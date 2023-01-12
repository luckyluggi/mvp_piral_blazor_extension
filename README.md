# Repro Steps
- `cd ./appshell` and run `npm i` and then `npm run build`
- `cd ../blazor-pilet` and run `dotnet build`
- `cd ../.piral~/blazor-pilet` and run `npm start`

# Problems
1. The Browser Console shows an error because `http://localhost:1234/$pilet-api/0/icons.dll` can't be found.
    The problem occours because in `icons\icons.csproj` we've added `<AssemblyName>Framework.Frontend.Icons</AssemblyName>`. This renames the dll to `Framework.Frontend.Icons.dll` but piral is still assuming the name `icons.dll`.
    The file `https://github.com/luckyluggi/mvp_piral_blazor_extension/blob/master/piral~/blazor-pilet/dist/_framework/Framework.Frontend.Icons.dll` does exist.
2. If i build with vite i get the following message when running the pilet: `The app shell does not contain `piral-blazor`. Using standalone mode.`
   It works when using webpack5.