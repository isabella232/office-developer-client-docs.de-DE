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
  
Wie in [MAPI-Nachrichtenklassen](mapi-message-classes.md)beschrieben, sind Nachrichtenklassen wichtig, um die Beziehung zwischen den Typen von benutzerdefinierten Nachrichten und nach der Erweiterung zwischen den Formular Servern selbst herzustellen. Glücklicherweise ist das Auswählen einer Nachrichtenklassen Zeichenfolge relativ einfach. Die Nachrichtenklassen Zeichenfolge einer Nachrichtenklasse ist eine beliebige Zeichenfolge, Sie sollte jedoch die folgenden Konventionen verwenden:
  
- Die Zeichenfolge sollte alle in der Dokumentation für die **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft beschriebenen Konventionen erfüllen. Wichtig ist, dass die Zeichenfolge vollständig aus ANSI-Zeichen bestehen muss und kleiner als 256 Zeichen ist.
    
- Wenn der Formularserver von einem vorhandenen Formularserver abgeleitet ist oder eine Erweiterung eines vorhandenen Formular Servers ist, sollte die Nachrichtenklassen Zeichenfolge durch Hinzufügen eines Punkts und eines anderen Wortes zur Nachrichtenklassen Zeichenfolge des Formular Servers, auf dem das Formular basiert, gebildet werden. Sie können beispielsweise ein Formular zum erneuten Planen einer Besprechung implementieren, und das Formular basiert auf einem vorhandenen Formular für die Planung von Besprechungen. Wenn die Nachrichtenklassen Zeichenfolge der Besprechungsplanung "IPM. "Meeting", die Nachrichtenklassen Zeichenfolge könnte "IPM" lauten. Besprechung. Umplanen ".
    
- Wenn das Formular nicht auf einem vorhandenen Formular basiert, sollte die Zeichenfolge der Nachrichtenklasse weiterhin mit dem "IPM." beginnen. oder "IPC". Prefix, je nachdem, ob das Formular von einer Person oder einer anderen Anwendung empfangen werden soll. "IPM." kennzeichnet eine zwischenmenschliche Nachricht, die normalerweise im Posteingang eines Benutzers landet, und "IPC". kennzeichnet eine Kommunikations Nachricht, die in der Regel nicht an den Posteingang eines Benutzers zugestellt wird.
    
- Wenn Ihre Nachrichtenklasse für den Benutzer lesbar ist, sollte die Nachrichtenklassen Zeichenfolge mit "IPM" beginnen. Eine Nachrichtenklasse wird allgemein als lesbar angesehen, wenn Sie Eigenschaften verwendet, die nur-Text-, HTML-oder Rich Text Format (RTF)-Daten enthalten. Wenn in Ihrem Formular die **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft verwendet wird, sollte es mit Sicherheit "IPM." verwenden. Nachrichtenklassen Zeichenfolge. Wenn Sie beispielsweise ein Formular für Bestellungen implementieren und Ihre Organisation erfordert, dass Bestellungen von einem Vorgesetzten genehmigt werden, könnte Ihre Nachrichtenklassen Zeichenfolge "IPM" lauten. Purchase_Order ". Formulare, die für die Verwendung mit öffentlichen Ordnern oder Anwendungen für Öffentliche Ordner entworfen wurden, werden in der Regel als Interpersonal betrachtet, da Sie von Personen gelesen werden, obwohl Sie nicht tatsächlich an die e-Mail-Adresse einer Person adressiert sind. Das typische Präfix für Nachrichtenklassen für Öffentliche Ordner lautet "IPM. Post ". 
    
- Wenn Ihre Nachrichtenklasse nicht von einer Person, sondern von einer anderen Anwendung empfangen werden soll, sollte die Nachrichtenklassen Zeichenfolge mit "IPC" beginnen. Wenn Sie beispielsweise ein Formular implementieren, mit dem Personen Mailinglisten automatisch abonnieren können, kann die Nachrichtenklassen Zeichenfolge "IPC" lauten. Subscribe ".
    
- Die Zeichenfolge der Nachrichtenklasse sollte nie mit einem Punkt enden.
    
Die Zeichenfolge der Nachrichtenklasse sollte im Abschnitt **[Description]** der Formular Konfigurationsdatei im **MessageClass** -Eintrag ähnlich der folgenden platziert werden: 
  
 `MessageClass=IPM.Meeting.Reschedule`
  
Nachdem Sie eine entsprechende Nachrichtenklassen Zeichenfolge ausgewählt haben, sollten Sie einen Klassenbezeichner dafür generieren. Klassen-IDs können mit dem Befehl **Create GUID** erstellt werden, der in Visual Studio enthalten ist. Der Klassenbezeichner muss in den **CLSID** -Eintrag der Formular Konfigurationsdatei eingefügt werden, zusammen mit dem **MessageClass** -Eintrag, ähnlich dem folgenden: 
  
 `CLSID={88FFF551-B8C5-11ce-8DE0-00AA0060D242}`
  
Ihre Klassen-ID ist natürlich sicherlich unterschiedlich. Weitere Informationen finden Sie unter [Creating a Form Configuration File](creating-a-form-configuration-file.md).
  
Wenn das Formular auf dem Computer eines Benutzers installiert ist, muss der Installationsprozess (unabhängig davon, ob es sich um ein Setupprogramm handelt) einen Registrierungseintrag im Abschnitt **\* HKEY_CLASSES_ROOT\CLSID* der Registrierung für den Klassenbezeichner erstellen. Dieser Eintrag muss auf die Zeichenfolge der Nachrichtenklasse festgelegt sein. Beispielsweise würden Sie einen Registrierungseintrag ähnlich der folgenden für die Beispiel-Klassen-ID oben erstellen: 
  
 `HKEY_CLASSES_ROOT\CLSID\{88FFF551-B8C5-11ce-8DE0-00AA0060D242}="IPM.Meeting.Reschedule"`
  
Weitere Informationen finden Sie unter [Installieren eines Formulars in einer Bibliothek](installing-a-form-into-a-library.md).
  
## <a name="see-also"></a>Siehe auch



[Entwickeln von MAPI-Formular Servern](developing-mapi-form-servers.md)

