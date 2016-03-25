A simple file chooser to android applications.

Possible add filters extensions, ex:
```
Intent intent = new Intent(this, FileChooser.class);
ArrayList<String> extensions = new ArrayList<String>();
extensions.add(".pdf");
extensions.add(".xls");
extensions.add(".xlsx");
intent.putStringArrayListExtra("filterFileExtension", extensions);
startActivityForResult(intent, FILE_CHOOSER);
```

Returns
```
@Override
public void onActivityResult(int requestCode, int resultCode, Intent data) {
    if ((requestCode == FILE_CHOOSER) && (resultCode == -1)) {
    	String fileSelected = data.getStringExtra("fileSelected");
    	Toast.makeText(this, fileSelected, Toast.LENGTH_SHORT).show();
    }    		
}
```

![https://lh3.googleusercontent.com/-6RoRJPyHxTM/TtmTO4L2RfI/AAAAAAAAA70/EBzuRjv9Nf4/s720/fileChooser.png](https://lh3.googleusercontent.com/-6RoRJPyHxTM/TtmTO4L2RfI/AAAAAAAAA70/EBzuRjv9Nf4/s720/fileChooser.png)