---
title: Auswählen einer Nachrichtenklasse
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5ca8edd2-41b7-40e2-b755-b28eecb49786
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cc7d2f6dc251a280738d2857e46a5d898fde3017
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556840"
---
# <a name="choosing-a-message-class"></a>Auswählen einer Nachrichtenklasse

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wie in [MAPI-Nachrichtenklassen](mapi-message-classes.md)beschrieben, sind Nachrichtenklassen wichtig, um die Beziehung zwischen benutzerdefinierten Nachrichtentypen und, durch Erweiterung, zwischen Formularservern selbst herzustellen. Glücklicherweise ist die Auswahl einer Nachrichtenklassenzeichenfolge ziemlich einfach. Die Nachrichtenklassenzeichenfolge einer Nachrichtenklasse ist eine beliebige Zeichenfolge, sie sollte jedoch die folgenden Konventionen verwenden:
  
- Die Zeichenfolge sollte alle Konventionen erfüllen, die in der Dokumentation für die **eigenschaft PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) beschrieben sind. Wichtig ist, dass die Zeichenfolge vollständig aus ANSI-Zeichen besteht und weniger als 256 Zeichen lang sein muss.
    
- Wenn der Formularserver von einem vorhandenen Formularserver abgeleitet ist oder eine Erweiterung eines vorhandenen Formularservers ist, sollte die Nachrichtenklassenzeichenfolge durch Hinzufügen eines Punkts und eines weiteren Worts zur Nachrichtenklassenzeichenfolge des Formularservers gebildet werden, auf dem das Formular basiert. Sie können z. B. ein Formular implementieren, um eine Besprechung neu zu planen, und ihr Formular basiert auf einem vorhandenen Formular zum Planen von Besprechungen. Wenn die Nachrichtenklassenzeichenfolge des Besprechungsplanungsformulars "IPM" lautet. "Meeting", your message class string could be "IPM. Meeting.Reschedule".
    
- Wenn das Formular nicht auf einem vorhandenen Formular basiert, sollte die Nachrichtenklassenzeichenfolge immer noch mit dem "IPM" beginnen. oder "IPC." präfix, je nachdem, ob das Formular von einer Person oder von einer anderen Anwendung empfangen werden soll. "IPM." bezeichnet eine zwischenmenschliche Nachricht, die in der Regel im Posteingang eines Benutzers endet, und "IPC". bezeichnet eine prozessübergreifende Kommunikationsnachricht, die in der Regel nicht an den Posteingang eines Benutzers übermittelt wird.
    
- Wenn ihre Nachrichtenklasse lesbar sein soll, sollte die Nachrichtenklassenzeichenfolge mit "IPM" beginnen. Eine Nachrichtenklasse gilt im Allgemeinen als lesbar, wenn sie Eigenschaften verwendet, die Nur-Text-, HTML- oder RTF-Daten (Rich Text Format) enthalten. Wenn Ihr Formular die **eigenschaft PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) verwendet, sollte es mit großer Wahrscheinlichkeit ein "IPM" verwenden. Nachrichtenklassenzeichenfolge. Wenn Sie z. B. ein Formular für Bestellungen implementieren und Ihre Organisation erfordert, dass Bestellungen von einem Vorgesetzten genehmigt werden, kann die Zeichenfolge der Nachrichtenklasse "IPM" sein. Purchase_Order". Formulare, die für die Verwendung mit öffentlichen Ordnern oder Anwendungen für öffentliche Ordner entwickelt wurden, werden in der Regel als zwischenmenschlich betrachtet, da sie von Personen gelesen werden, obwohl sie eigentlich nicht an die E-Mail-Adresse einer Person adressiert sind. Das typische Präfix für Nachrichtenklassen für öffentliche Ordner ist "IPM. Post". 
    
- Wenn Ihre Nachrichtenklasse von einer anderen Anwendung anstelle von einer Person empfangen werden soll, sollte die Nachrichtenklassenzeichenfolge mit "IPC" beginnen. Wenn Sie z. B. ein Formular implementieren, das es Personen ermöglicht, Mailinglisten automatisch zu abonnieren, könnte ihre Nachrichtenklassenzeichenfolge "IPC" sein. Abonnieren".
    
- Die Nachrichtenklassenzeichenfolge sollte niemals mit einem Punkt enden.
    
Die Zeichenfolge der Nachrichtenklasse sollte im Abschnitt **[Beschreibung]** der Formularkonfigurationsdatei im **MessageClass-Eintrag** platziert werden, ähnlich wie der folgende: 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
Nachdem Sie eine entsprechende Nachrichtenklassenzeichenfolge ausgewählt haben, sollten Sie einen Klassenbezeichner dafür generieren. Klassenbezeichner können mit dem **Befehl GUID** erstellen generiert werden, der in Visual Studio enthalten ist. Der Klassenbezeichner muss zusammen mit dem **MessageClass-Eintrag** in den **CLSID-Eintrag** der Formularkonfigurationsdatei eingefügt werden, ähnlich wie der folgende: 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
Der Klassenbezeichner wird natürlich mit großer Sicherheit anders sein. Weitere Informationen finden Sie unter [Erstellen einer Formularkonfigurationsdatei.](creating-a-form-configuration-file.md)
  
Wenn das Formular auf dem Computer eines Benutzers installiert ist, muss ihr Installationsprozess – ob es sich um ein Setupprogramm oder ein anderes Handelt – einen Registrierungseintrag im **HKEY_CLASSES_ROOT\CLSID\** Abschnitt der Registrierung für den Klassenbezeichner vornehmen. Dieser Eintrag muss auf die Nachrichtenklassenzeichenfolge festgelegt werden. Sie würden z. B. einen Registrierungseintrag ähnlich dem folgenden für den obigen Beispielklassenbezeichner erstellen: 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
Weitere Informationen finden Sie unter [Installieren eines Formulars in einer Bibliothek.](installing-a-form-into-a-library.md)
  
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

