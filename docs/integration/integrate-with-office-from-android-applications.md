---
title: Integration in Office von Android-Anwendungen aus
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a765fa49-a272-4047-9147-59cc68e5dd27
description: Office für Android bietet eine erweiterbare Lösung, die die Integration in Drittanbieteranwendungen ermöglicht. Von Ihrer Android-Anwendung aus ist eine Integration in Office möglich, indem Sie Ihre Anwendungsbenutzer an Office übergeben.
ms.openlocfilehash: 4e674b3d66f3acba7e9c9c19e716ff0d73d803b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393026"
---
# <a name="integrate-with-office-from-android-applications"></a>Integration in Office von Android-Anwendungen aus

Office für Android bietet eine erweiterbare Lösung, die die Integration in Drittanbieteranwendungen ermöglicht. Von Ihrer Android-Anwendung aus ist eine Integration in Office möglich, indem Sie Ihre Anwendungsbenutzer an Office übergeben.
  
Sie können Benutzern, die Office auf Android-Geräten ausführen, das Öffnen und Bearbeiten von in SharePoint oder OneDrive gespeicherten Dateien von einer beliebigen Anwendung aus ermöglichen. Übergeben Sie dazu mit dem Protokollhandler die Dateien an Office, und stellen Sie sicher, dass Office so aufgerufen wird, dass Office dies versteht.
  
Wenn ein Benutzer das Bearbeiten einer Datei abgeschlossen hat, kann er „ZURÜCK" wählen, um zur ursprünglichen Speicheranwendung zurückzukehren.
  
## <a name="verify-that-office-has-been-installed"></a>Sicherstellen, dass Office installiert wurde

Die verweisende Anwendung muss zunächst überprüfen, dass eine bestimmte Office-Anwendung installiert ist. Die folgenden Office-Anwendungen können auf Android-Geräten zum Anzeigen und Bearbeiten von Dokumenten installiert werden: 
  
- Excel
    
- PowerPoint
    
- Word
    
Verwenden Sie PackageManager von Android, um zu ermitteln, ob eine bestimmte Office-Anwendung auf dem Gerät installiert ist. In der folgenden Tabelle sind die Paketnamen für Office-Anwendungen aufgeführt, die Sie in diesem Prozess verwenden können.
  
|**Anwendung**|**Name des Pakets**|
|:-----|:-----|
|Excel  <br/> |com.microsoft.office.excel  <br/> |
|PowerPoint  <br/> |com.microsoft.office.powerpoint  <br/> |
|Word  <br/> |com.microsoft.office.word  <br/> |
   
### <a name="prompt-the-user-to-install-office"></a>Auffordern des Benutzers zur Installation von Office

Wenn eine bestimmte Office-Anwendung nicht installiert ist, kann der Benutzer zum Installieren der Anwendung aufgefordert werden. In der folgenden Tabelle sind die verfügbaren Installationsorte für Office-Anwendungen aufgeführt.
  
|**Anwendung**|**Google Play Store**|
|:-----|:-----|
|Excel  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.excel](https://play.google.com/store/apps/details?id=com.microsoft.office.excel) <br/> |
|PowerPoint  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint](https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint) <br/> |
|Word  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.word](https://play.google.com/store/apps/details?id=com.microsoft.office.word) <br/> |
   
## <a name="invoke-office"></a>Aufrufen von Office

Wenn die Office-Anwendung installiert ist, kann die verweisende Anwendung Office durch Übergeben der folgenen Details aufrufen:
  
- Office-Protokoll
    
- Open-Modus
    
- URL
    
Schemaformat:
  
 `<Office protocol><open mode>|u|<URL>`
  
Das folgende Beispiel zeigt eine Anforderung zum Aufrufen einer Word-Datei zur Bearbeitung:
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx`
  
### <a name="office-protocols"></a>Office-Protokolle

Die folgende Tabelle enthält die Protokolle für jede Office-Anwendung.
  
|**Anwendung**|**Protocol**|
|:-----|:-----|
|Excel  <br/> |ms-excel:  <br/> |
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
  
## <a name="see-also"></a>Siehe auch
<a name="bk_addresources"> </a>

- [Integration in Office](integrate-with-office.md)
    
- [PackageManager](https://developer.android.com/reference/android/content/pm/PackageManager.html)
    
- [GetPackageManager()](https://developer.android.com/reference/android/content/Context.html)
    

