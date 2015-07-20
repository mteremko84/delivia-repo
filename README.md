# delivia-repo
coursera data scientist tool box


pollutantmean <- function(directory=getwd("C:/Users/larry/Desktop/specdata"), pollutant, id = 1:332) {
+     fileList = list.files(path)
+     file_names = as.numeric(sub("\\.csv$","",fileList))
+     selected_files = fileList[match(id,file_names)]
+     pollutantData = lapply(file.path(path,selected_files),read.csv)
+     pollutantData = do.call(rbind.data.frame,pollutantData)
+     mean(pollutantData[,pollutant],na.rm=TRUE)
+ }