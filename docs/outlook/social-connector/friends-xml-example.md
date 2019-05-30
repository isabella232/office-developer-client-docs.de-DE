---
title: XML-Beispiel für „friends“
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: 'Das XML-Beispiel in diesem Thema ist eine Friend-XML-Zeichenfolge, die an die Connector für soziale Netzwerke (OSC) zurückgegeben wird, nachdem Sie die ISocialPerson:: GetFriendsAndColleagues-Methode aufgerufen hat. Das Beispiel zeigt die Friends-XML für zwei Freunde, die jeweils durch das Person-Element getrennt werden. Jeder Friend gibt einen eindeutigen Wert für das UserID-Element im sozialen Netzwerk an.'
ms.openlocfilehash: 593019ec4dcd1b9b578bfe275fb8e6664bbd11a9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542226"
---
# <a name="friends-xml-example"></a>XML-Beispiel für „friends“

Das XML-Beispiel in diesem Thema ist eine Friend-XML-Zeichenfolge, die an die Connector für soziale Netzwerke (OSC) zurückgegeben wird, nachdem Sie die [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) -Methode aufgerufen hat. Das Beispiel zeigt die **friends** -XML für zwei Freunde, die jeweils durch das **Person** -Element getrennt werden. Jeder Friend gibt einen eindeutigen Wert für das **UserID** -Element im sozialen Netzwerk an. 
  
Die restlichen Elemente des **friends** -XML weisen selbsterklärende Namen auf. Eine ausführliche Beschreibung dieser Elemente finden Sie unter [XML for friends](xml-for-friends.md). 
  
## <a name="xml-example"></a>XML-Beispiel

Das folgende Beispiel zeigt die XML- **Freunde** für zwei Personen im sozialen Netzwerk. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<friends xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <person>
    <userID>4667647</userID>
    <firstName>Melissa</firstName>
    <lastName>MacBeth</lastName>
    <nickname></nickname>
    <fileAs>MacBeth, Melissa (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Product Manager</title>
    <anniversary>2005-05-17</anniversary>
    <birthday>1979-08-09</birthday>
    <emailAddress>melissa@contoso.com</emailAddress>
    <emailAddress2>melissa@fabrikam.com</emailAddress2>
    <emailAddress3>melissa@adventureworks.com</emailAddress3>
    <webProfilePage>https://contoso.com/melissa</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>female</gender>
    <index>0</index>
  </person>
  <person>
    <userID>5015012</userID>
    <firstName>Michael</firstName>
    <lastName>Affronti</lastName>
    <nickname>Mr. Social</nickname>
    <fileAs>Affronti, Michael (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Sales Director</title>
    <anniversary>2009-06-21</anniversary>
    <birthday>1980-09-10</birthday>
    <emailAddress>michael@contoso.com</emailAddress>
    <emailAddress2>michael@fabrikam.com</emailAddress2>
    <emailAddress3>michael@adventureworks.com</emailAddress3>
    <webProfilePage>https://contoso.com/michael</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>male</gender>
    <index>1</index>
  </person>
</friends>

```

## <a name="see-also"></a>Siehe auch

- [XML-Beispiele für osc-Anbieter](osc-provider-xml-examples.md)  
- [XML-Beispiel für Funktionen](capabilities-xml-example.md) 
- [XML-Beispiel für Aktivitätsfeeds](activity-feed-xml-example.md) 
- [Connector für soziale Netzwerke Anbieter-XML-Schema](outlook-social-connector-provider-xml-schema.md)

