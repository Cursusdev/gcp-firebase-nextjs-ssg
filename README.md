# run command local environnemnt  
$ docker build . --tag eu.gcr.io/gcp-host-ssr/nextjs-blog:latest  

$ docker run -p 8085:3000 eu.gcr.io/gcp-host-ssr/nextjs-blog:latest  

$ docker push eu.gcr.io/gcp-host-ssr/nextjs-blog:latest  

# transfert to GCR
// $ gcloud auth configure-docker  
$ gcloud builds submit --tag eu.gcr.io/gcp-host-ssr/nextjs-blog:latest  

# deploy to Cloud Run  
$ gcloud beta run deploy --image eu.gcr.io/gcp-host-ssr/nextjs-blog:latest  

$ firebase deploy --only hosting  

// source ssg: https://firebase.googleblog.com/2019/04/  firebase-hosting-and-cloud-run.html  
