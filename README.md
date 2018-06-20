# JavaBase64ImageValidator
```Java
public boolean isValidBase64Image(String imgInBase64){
	BufferedImage image = null;
	byte [] imgBytes = java.util.Base64.getDecoder().decode(imgInBase64);
	try(ByteArrayInputStream bis = new ByteArrayInputStream(imgBytes)) {
		image = ImageIO.read(bis);
	} catch (IOException e) {
		e.printStackTrace();
		return false;
	}
	return image != null;
}
```
