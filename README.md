# Repro Steps
- `cd ./appshell` and run `npm i` and then `npm run build`
- `cd ../blazor-pilet` and run `dotnet build`
- `cd ../.piral~/blazor-pilet` and run `npm start`

# Problems
1. The Logo Extension is not loaded `blazor-pilet\Components\Logo.razor`
2. If i build with vite i get the following message when running the pilet: `The app shell does not contain `piral-blazor`. Using standalone mode.`
   It works when using webpack5