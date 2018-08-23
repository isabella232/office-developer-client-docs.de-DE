---
title: Auswählen einer Nachrichtenklasse
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ca8edd2-41b7-40e2-b755-b28eecb49786
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c3b486838c6ce2d7fc38d950a4de6f4589767073
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574237"
---
# <a name="choosing-a-message-class"></a>Auswählen einer Nachrichtenklasse

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wie im [MAPI-Nachrichtenklassen](mapi-message-classes.md)beschrieben, sind Nachrichtenklassen wichtig für die Beziehung zwischen verschiedenen Arten von benutzerdefinierten Nachrichten und durch Erweiterung, zwischen Formular Server selbst herstellen. Auswählen einer Klasse Meldungszeichenfolge ist zum Glück relativ einfach. Die Klasse Meldungszeichenfolge einer Nachrichtenklasse ist eine beliebige Zeichenfolge, jedoch sollten Sie die folgenden typografischen Konventionen verwenden:
  
- Die Zeichenfolge sollten alle in der Dokumentation für die Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) beschriebenen Konventionen zu erfüllen. Die Zeichenfolge muss vor allem vollständig aus ANSI-Zeichen bestehen und kleiner als 256 Zeichen lang sein.
    
- Ihr Formular Server wird von einem vorhandenen Formular Server abgeleitet oder ist eine Erweiterung eines vorhandenen Formulars Servers, sollte Ihre Klasse Meldungszeichenfolge gebildet werden durch Hinzufügen von einem Punkt und anderen Worts auf die Klasse Meldungszeichenfolge des Formular-Servers, der das Formular basiert. Beispielsweise möglicherweise möchten Sie ein Formular, um eine Besprechung erneut planen, implementieren und Ihr Formular basiert auf einem vorhandenen Formular zum Planen von Besprechungen. Ist die Besprechung planen des Formulars Meldungszeichenfolge-Klasse "IPM. Besprechung", könnte Ihre Klasse Meldungszeichenfolge"IPM. Meeting.Reschedule".
    
- Wenn das Formular nicht auf alle vorhandenen Formular basiert, sollte Ihre Klasse Meldungszeichenfolge weiterhin mit entweder die "IPM." beginnen oder "IPK" Präfix, je nachdem, ob das Formular von einer Person oder einer anderen Anwendung empfangen werden soll. "IPM." Legt eine zwischen Personen an, die in der Regel im Posteingang des Benutzers und "IPK" endet Legt eine prozessübergreifenden Kommunikation an, die nicht in der Regel an den Posteingang eines Benutzers übermittelt wird.
    
- Wenn Ihre Nachrichtenklasse lesbar sein soll, sollten die Klasse Meldungszeichenfolge mit "IPM." beginnen. Eine Nachrichtenklasse wird im Allgemeinen als lesbare, wenn es Eigenschaften verwendet, die nur-Text, HTML, enthalten oder Rich Text Format (RTF)-Daten. Wenn das Formular die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft verwendet wird, sollte fast immer "IPM." verwendet werden Zeichenfolge-Klasse. Angenommen, wenn Sie ein Formular für Bestellungen implementieren, und Ihre Organisation erfordert, dass eine Bestellung von einem Manager genehmigt werden, könnte Ihre Klasse Meldungszeichenfolge "IPM. Purchase_Order". Formulare, die für die vorgesehen sind mit öffentlichen Ordnern verwenden oder Öffentliche Ordner Anwendungen werden in der Regel als zwischen Personen sein, da sie von Personen gelesen werden, obwohl sie tatsächlich nicht an die e-Mail-Adresse einer Person adressiert sind. Typische Präfix für Öffentliche Ordner-Nachrichtenklassen lautet "IPM. POST". 
    
- Wenn Ihre Nachrichtenklasse von einer anderen Anwendung anstelle von empfangen werden von einer Person vorgesehen ist, sollte die Klasse Meldungszeichenfolge mit "IPK" beginnen. Beispielsweise wenn Sie ein Formular, mit dem Personen automatisch Adressenlisten abonnieren können implementieren, könnte Ihre Klasse Meldungszeichenfolge "IPK Abonnieren Sie".
    
- Ihre Klasse Meldungszeichenfolge sollte niemals mit einem Punkt enden.
    
Platzieren Sie die Klasse Meldungszeichenfolge im Abschnitt **[Beschreibung]** der Konfigurationsdatei Formular im **MessageClass** -Eintrag, ähnlich der folgenden: 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
Nachdem Sie eine entsprechende Meldung Klasse Zeichenfolge ausgewählt haben, sollten Sie dafür ein Klassenbezeichner erstellen. Klassenbezeichner können mit dem Befehl **GUID erstellen** , die in Visual Studio enthalten ist, generiert werden. Platzieren Sie die Klassen-ID in der Konfigurationsdatei Formular **CLSID** -Eintrag, zusammen mit den **MessageClass** -Eintrag, ähnlich der folgenden: 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
Die Klassen-ID wird sehr wahrscheinlich natürlich unterschiedlich sein. Weitere Informationen finden Sie unter [Erstellen einer Konfigurationsdatei Formular](creating-a-form-configuration-file.md).
  
Wenn das Formular auf dem Computer eines Benutzers, der Installationsvorgang installiert wird – gibt an, ob es sich um ein Setup-Programm oder etwas anderes ist – müssen in einen Registrierungseintrag, der **HKEY_CLASSES_ROOT\CLSID\* * -Abschnitts der Registrierung für die Klassen-ID. Bei diesem Eintrag muss auf die Klasse Meldungszeichenfolge festgelegt werden. Beispielsweise würden Sie einen Registrierungseintrag ähnlich dem folgenden für die oben genannten Beispiel Klassenbezeichner erstellen: 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
Weitere Informationen finden Sie unter [Installieren eines Formulars in eine Bibliothek](installing-a-form-into-a-library.md).
  
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

