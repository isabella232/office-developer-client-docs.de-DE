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
ms.openlocfilehash: 279df7f07c8c8b66347488c6224d04f70292e968
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428053"
---
# <a name="choosing-a-message-class"></a>Auswählen einer Nachrichtenklasse

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wie in [MAPI-Nachrichtenklassen](mapi-message-classes.md)beschrieben, sind Nachrichtenklassen wichtig, um die Beziehung zwischen Benutzerdefinierten Nachrichtentypen und durch Erweiterung zwischen Formularservern selbst zu erstellen. Glücklicherweise ist die Auswahl einer Nachrichtenklassenzeichenfolge ziemlich einfach. Die Nachrichtenklassenzeichenfolge einer Nachrichtenklasse ist eine beliebige Zeichenfolge, sollte jedoch die folgenden Konventionen verwenden:
  
- Die Zeichenfolge sollte alle in der Dokumentation für die eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) beschriebenen Konventionen erfüllen. Wichtig ist, dass die Zeichenfolge vollständig aus ANSI-Zeichen bestehen muss und weniger als 256 Zeichen lang sein muss.
    
- Wenn Der Formularserver von einem vorhandenen Formularserver abgeleitet ist oder eine Erweiterung eines vorhandenen Formularservers ist, sollte die Nachrichtenklassenzeichenfolge durch Hinzufügen eines Zeitraums und eines anderen Worts zur Nachrichtenklassenzeichenfolge des Formularservers gebildet werden, auf dem Ihr Formular basiert. Sie können z. B. ein Formular implementieren, um eine Besprechung neu zu planen, und Ihr Formular basiert auf einem vorhandenen Formular zum Planen von Besprechungen. Wenn die Nachrichtenklassenzeichenfolge des Besprechungsplanungsformulars "IPM. Besprechung", könnte ihre Nachrichtenklassenzeichenfolge "IPM. Meeting.Reschedule".
    
- Wenn Ihr Formular nicht auf einem vorhandenen Formular basiert, sollte ihre Nachrichtenklassenzeichenfolge weiterhin mit dem "IPM" beginnen. oder "IPC". Präfix, je nachdem, ob das Formular von einer Person oder einer anderen Anwendung empfangen werden soll. "IPM". bezeichnet eine zwischenpersonelle Nachricht, die in der Regel im Posteingang eines Benutzers landet, und "IPC". legt eine Kommunikationsnachricht zwischen den Verarbeitungsprozessen fest, die in der Regel nicht an den Posteingang eines Benutzers zugestellt wird.
    
- Wenn Ihre Nachrichtenklasse für den Menschen lesbar sein soll, sollte die Zeichenfolge der Nachrichtenklasse mit "IPM" beginnen. Eine Nachrichtenklasse wird im Allgemeinen als menschlich lesbar betrachtet, wenn sie Eigenschaften verwendet, die Nur-Text-, HTML- oder Rich Text Format (RTF)-Daten enthalten. Wenn Ihr Formular die **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft verwendet, sollte es mit sicherheit ein "IPM" verwenden. Nachrichtenklassenzeichenfolge. Wenn Sie beispielsweise ein Formular für Bestellungen implementieren und Ihre Organisation erfordert, dass Bestellungen von einem Vorgesetzten genehmigt werden, kann ihre Nachrichtenklassenzeichenfolge "IPM" sein. Purchase_Order". Formulare, die für die Verwendung mit öffentlichen Ordnern oder Anwendungen für öffentliche Ordner entwickelt wurden, gelten in der Regel als interpersonal, da sie von Personen gelesen werden, obwohl sie nicht an die E-Mail-Adresse einer Person adressiert sind. Das typische Präfix für Nachrichtenklassen für öffentliche Ordner lautet "IPM. Post". 
    
- Wenn Ihre Nachrichtenklasse von einer anderen Anwendung statt von einer Person empfangen werden soll, sollte die Nachrichtenklassenzeichenfolge mit "IPC" beginnen. Wenn Sie z. B. ein Formular implementieren, mit dem Benutzer Mailinglisten automatisch abonnieren können, könnte ihre Nachrichtenklassenzeichenfolge "IPC" sein. Subscribe".
    
- Ihre Nachrichtenklassenzeichenfolge sollte niemals mit einem Zeitraum enden.
    
Die Zeichenfolge der Nachrichtenklasse sollte im **Abschnitt [Beschreibung]** der Formularkonfigurationsdatei im **Eintrag MessageClass** wie folgt angezeigt werden: 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
Nachdem Sie eine entsprechende Nachrichtenklassenzeichenfolge ausgewählt haben, sollten Sie einen Klassenbezeichner dafür generieren. Klassenbezeichner können mit dem Befehl **GUID erstellen** generiert werden, der in der Visual Studio. Der Klassenbezeichner muss im **CLSID-Eintrag** der Formularkonfigurationsdatei zusammen mit dem **MessageClass-Eintrag** wie folgt angegeben werden: 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
Ihre Klassen-ID ist natürlich mit sicherheit unterschiedlich. Weitere Informationen finden Sie unter [Creating a Form Configuration File](creating-a-form-configuration-file.md).
  
Wenn das Formular auf dem Computer eines Benutzers installiert ist, muss ihr Installationsvorgang – unabhängig davon, ob es sich um ein Setupprogramm oder einen anderen Vorgang handelt – einen Registrierungseintrag im Abschnitt **HKEY_CLASSES_ROOT\CLSID\** der Registrierung für die Klassen-ID vornehmen. Dieser Eintrag muss auf die Nachrichtenklassenzeichenfolge festgelegt werden. Beispielsweise würden Sie einen Registrierungseintrag wie den folgenden für den obigen Beispielklassenbezeichner erstellen: 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
Weitere Informationen finden Sie unter [Installing a Form into a Library](installing-a-form-into-a-library.md).
  
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formularservern](developing-mapi-form-servers.md)

