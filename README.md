# SharagaPR17
1 Код для отправки письма:
Uri uri = Uri.parse("mailto:xxx@abc.com");
Intent it = new Intent(Intent.ACTION_SENDTO, uri);
startActivity(it);
Intent it = new Intent(Intent.ACTION_SEND);   
it.putExtra(Intent.EXTRA_EMAIL, "me@abc.com");   
it.putExtra(Intent.EXTRA_TEXT, "The email body text");   
it.setType("text/plain");   
startActivity(Intent.createChooser(it, "Choose Email Client"));   
Intent it=new Intent(Intent.ACTION_SEND);   
String[] tos={"me@abc.com"};   
String[] ccs={"you@abc.com"};   
it.putExtra(Intent.EXTRA_EMAIL, tos);   
it.putExtra(Intent.EXTRA_CC, ccs);   
it.putExtra(Intent.EXTRA_TEXT, "The email body text");   
it.putExtra(Intent.EXTRA_SUBJECT, "The email subject text");   
it.setType("message/rfc822");   
startActivity(Intent.createChooser(it, "Choose Email Client"));   






2 Код для добавления вложения:
Intent it = new Intent(Intent.ACTION_SEND);   
it.putExtra(Intent.EXTRA_SUBJECT, "The email subject text");   
it.putExtra(Intent.EXTRA_STREAM, "file:///sdcard/mysong.mp3");   
sendIntent.setType("audio/mp3");   
startActivity(Intent.createChooser(it, "Choose Email Client"));

3 Код для удаления программы:
Uri uri = Uri.fromParts("package", strPackageName, null);   
Intent it = new Intent(Intent.ACTION_DELETE, uri);   
startActivity(it);

4 Построить план маршрута:
Uri uri = Uri.parse("http://maps.google.com/maps?f=d&saddr=startLat%20startLng&daddr=endLat%20endLng&hl=en");
Intent it = new Intent(Intent.ACTION_VIEW,URI);
startActivity(it);
