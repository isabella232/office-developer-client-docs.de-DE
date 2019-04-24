---
title: Integration in Office von iOS-Anwendungen aus
manager: soliver
ms.date: 06/04/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f3a277ba-7ba1-4eea-83b5-915b409f3093
description: Office für iOS bietet eine erweiterbare Lösung, die die Integration in Drittanbieteranwendungen ermöglicht. Dieser Artikel beschreibt, wie Sie eine Integration in Office von Ihrer iOS-Anwendung ausführen können, indem Sie Benutzer von Ihrer Anwendung in Office übergeben und sie dann an die Anwendung zurückgeben.
ms.openlocfilehash: d17a096c17eadab0cd94ee1dce18e979e80fa65d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299748"
---
# <a name="integrate-with-office-from-ios-applications"></a>Integration in Office von iOS-Anwendungen aus

Office für iOS bietet eine erweiterbare Lösung, die die Integration in Drittanbieteranwendungen ermöglicht. Dieser Artikel beschreibt, wie Sie eine Integration in Office von Ihrer iOS-Anwendung ausführen können, indem Sie Benutzer von Ihrer Anwendung in Office übergeben und sie dann an die Anwendung zurückgeben.
  
Sie können Benutzern, die Office auf einem iOS-Gerät ausführen, ermöglichen, Dateien, die in SharePoint oder OneDrive gespeichert sind, von einer beliebigen Anwendung aus zu öffnen und zu bearbeiten und sie dann schnell in die ursprüngliche Anwendung zurückzugeben, wenn sie das Bearbeiten der Datei abgeschlossen haben. Hierfür übergeben Sie Dateien über Protokollhandler an Office und stellen sicher, dass Office so aufgerufen wird, dass Office dies versteht.
  
Wenn ein Benutzer mit der Bearbeitung einer Datei fertig ist, kann er auf den Pfeil "Zurück" in der Office-Anwendung klicken, um das Dokument zu schließen und es an die ursprüngliche Speicheranwendung zurückzugeben, vorausgesetzt, Sie übergeben bestimmte Informationen an die Office-Anwendung, wenn diese gestartet wird.
  
## <a name="verify-that-office-has-been-installed"></a>Überprüfen, dass Office installiert wurde

Die verweisende Anwendung muss zunächst überprüfen, dass eine bestimmte Office-Anwendung installiert ist. Die folgenden Office-Anwendungen können auf iOS-Geräten zum Anzeigen und Bearbeiten von Dokumenten installiert werden:
  
- Excel
    
- OneNote
    
- PowerPoint
    
- Word
    
Verwenden Sie die [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)-Methode, um zu bestimmen, ob die Anwendung die Ressourcen öffnen kann. Diese Methode verwendet die URL für die Ressource als Parameter und gibt **No** zurück, wenn die Anwendung, die die URL akzeptiert, nicht verfügbar ist. Wenn **canOpenURL** den Text **No** zurückgibt, müssen Sie den Benutzer auffordern, Office zu installieren.
  
### <a name="prompt-the-user-to-install-office"></a>Auffordern des Benutzers zur Installation von Office

 Wenn eine bestimmte Office-Anwendung nicht installiert ist, können Sie ein [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)-Objekt verwenden, um den iTunes App Store in Ihrer Anwendung zu rendern und dem Benutzer die zu installierende Office-Anwendung anzuzeigen. In der folgenden Tabelle sind die jeweiligen iTunes-IDs aufgeführt, die für das Aufrufen der einzelnen Office-Anwendungen im Store Kit Product View Controller verwendet werden. 
  
|**Office-Anwendung**|**iTunes-ID**|
|:-----|:-----|
|Excel  <br/> |[https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4) <br/> |
|OneNote (iPhone)  <br/> |[https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4) <br/> |
|PowerPoint  <br/> |[https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4) <br/> |
|Word  <br/> |[https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4) <br/> |
   
## <a name="invoke-office"></a>Aufrufen von Office

Wenn die Office-Anwendung installiert ist, kann die verweisende Anwendung Office durch Übergeben der folgenen Details aufrufen: 
  
- Office-Protokoll
    
- Open-Modus
    
- URL
    
- Passback-Protokoll
    
- Dokumentenkontext
    
Schemaformat:
  
 `<Office protocol><open mode>|u|<URL>|p|<passback protocol>|c|<document context>`
  
Das folgende Beispiel zeigt eine Anforderung zum Aufrufen einer Word-Datei zur Bearbeitung:
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx|p|clouddrive|c|folderviewQ4`
  
### <a name="office-protocols"></a>Office-Protokolle

Die folgende Tabelle enthält die Protokolle für jede Office-Anwendung. 
  
|**Anwendung**|**Protokoll**|
|:-----|:-----|
|Excel  <br/> |ms-excel:  <br/> |
|OneNote  <br/> |onenote:  <br/> |
|PowerPoint  <br/> |ms-powerpoint:  <br/> |
|Word  <br/> |ms-word:  <br/> |
   
### <a name="open-mode"></a>Open-Modus

Office-Anwendungen können Dateien direkt im Ansichtsmodus (ofv) oder im Bearbeitungsmodus (ofe) öffnen. Der Bearbeitungsmodus ist Standard. 
  
Schemaformat:
  
 `<ofv or ofe>`
  
### <a name="url"></a>URL

Die URL besteht aus drei Teilen: 
  
- Der Deklaration, dass die Datei zum Bearbeiten geöffnet wird (ofe)
    
- Dem URL-Deskriptor (|u|)
    
- Der URL
    
Die URL muss codiert sein und muss eine direkte Verbindung zu der Datei (keine Umleitung) sein. Wenn die URL ein Format aufweist, das Office nicht verarbeiten kann, oder einfach ein Downloadfehler auftritt, gibt Office den Benutzer nicht an die aufrufende Anwendung zurück. 
  
Schemaformat:
  
 `|u|<document URL>`
  
### <a name="passback-protocol-optional"></a>Passback-Protokoll (optional)

Wenn Sie möchten, dass Office Benutzer an Ihre iOS-Anwendung zurückgibt, wenn diese auf den Pfeil "Zurück" klicken, muss die aufrufende Anwendung das Passback-Protokoll verwenden, das den Deskriptor '|p|' gefolgt vom App-Protokoll (ohne Doppelpunkt) umfasst. Sie müssen sicherstellen, dass die Anwendung die Antwort von Office korrekt verarbeiten kann.
  
Schemaformat:
  
 `|p|<passback protocol>`
  
### <a name="document-context-optional"></a>Dokumentenkontext (optional)

Office verwendet den Dokumentkontext nicht, die verweisende Anwendung benötigt diesen jedoch möglicherweise, wenn Office einen Benutzer zurückgibt. Wenn Sie möchten, dass der Dokumentkontext an Ihre Anwendung zurückgegeben wird, verwenden Sie den Deskriptor '|c|' gefolgt von dem gewünschten Kontext als Zeichenfolge. In Office gibt es (abgesehen von den Beschränkungen des Betriebssystems ) keine Längenbeschränkung für die Zeichenfolge.
  
Schemaformat:
  
 `|c|<document context>`
  
## <a name="return-users-to-the-referring-application"></a>Zurückgeben von Benutzern an die verweisende Anwendung

Aus Sicherheitsgründen gibt Office nur Benutzer an die verweisende Andwendung zurück, wenn die Datei erfolgreich geöffnet wurde. Wenn der Benutzer den Pfeil "Zurück" auswählt, antwortet Office der aufrufenden Anwendung mit dem Passback-Protokoll, dem Open-Modus, der URL, dem ausstehenden Uploadstatus und dem Dokumentkontext. Der ausstehende Uploadstatus verwendet den Deskriptor |z| und ist entweder "ja" oder "nein".
  
Schemaformat:
  
 `<app protocol>:ofe|u|<URL>|z|<yes or no>|c|<doc context> Example: clouddrive:ofe|u|https://contoso/Q4/budget.docx|z|no|c|folderviewQ4`
  
## <a name="see-also"></a>Siehe auch
<a name="bk_addresources"> </a>

- [canOpenURL-Methode](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [UIApplication-Klasse](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [SKProductViewController-Objekt](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)
    

