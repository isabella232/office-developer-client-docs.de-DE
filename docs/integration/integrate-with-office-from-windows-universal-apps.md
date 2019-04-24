---
title: Integration in Office von universellen Windows-Apps aus
manager: soliver
ms.date: 02/06/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60b4fa23-0075-4f6a-8bd0-9e53e99432d5
description: Sie können Ihre Drittanbieter-Apps für die universelle Windows-App-Plattform in Excel Mobile, PowerPoint Mobile und Word Mobile integrieren. Universelle Apps lassen sich in Office-Apps über Windows-Verträge für die Dateiauswahl, Expando-Eigenschaften und Contracts für die Aktualisierung zwischengespeicherter Dateien integrieren.
ms.openlocfilehash: ad04ccc3ceb6e0f1d53e4aebc12cf9724ab8ab66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299768"
---
# <a name="integrate-with-office-from-windows-universal-apps"></a>Integration in Office von universellen Windows-Apps aus

Sie können Ihre Drittanbieter-Apps für die universelle Windows-App-Plattform in Excel Mobile, PowerPoint Mobile und Word Mobile integrieren. Universelle Apps lassen sich in Office-Apps über Windows-[Verträge für die Dateiauswahl](https://msdn.microsoft.com/library/windows/apps/hh465174.aspx), [Expando-Eigenschaften](https://msdn.microsoft.com/library/windows/apps/xaml/hh770655.aspx) und [Contracts für die Aktualisierung zwischengespeicherter Dateien](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx) integrieren.
  
Wenn Sie Ihre universelle App in Excel, PowerPoint oder Word Mobile integrieren, können Benutzer von der App bereitgestellte Office-Dokumente öffnen, wenn sie innerhalb von Office suchen oder mit Windows Dateien in Ihrer App öffnen. Benutzer können die Datei auch wieder in der universellen App speichern, wodurch die Datei wieder zu Ihrem Dienst hochgeladen wird.
  
Auf diese Weise geöffnete Dateien werden in der Liste der zuletzt verwendeten Dokumente in Office angezeigt, damit die Benutzer sie leicht finden und wieder öffnen können.
  
Für diese Integration muss die universelle App folgende Bedingungen erfüllen:
    
- Sie implementiert die Windows-[Verträge für die Dateiauswahl](https://msdn.microsoft.com/library/windows/apps/hh465174.aspx).
    
- Sie stellt einen Dateispeicher dar (z. B. eine App, die Zugriff auf Cloud-Speicher ermöglicht).
    
## <a name="expando-properties"></a>Expando-Eigenschaften

Universelle Windows-Apps können über Expando-Eigenschaften weitere Informationen kommunizieren, die mit Dateien verknüpft sind. Informationen dazu, wie dies in Windows funktioniert, finden Sie unter „System.ExpandoProperties" in [StorageItemContentProperties.SavePropertiesAsync](https://msdn.microsoft.com/library/windows/apps/xaml/hh770655.aspx).
  
In der folgenden Tabelle sind die Eigenschaften beschrieben, die Ihre App Office zur Verfügung stellen muss, um Dateiöffnungsszenarien zu unterstützen. Werden diese Informationen nicht bereitgestellt, werden alle Dateien aus Ihrer App schreibgeschützt geöffnet. Ob Benutzer Dateien zum Bearbeiten öffnen können, hängt vom Typ der Office-Lizenz ab, die sie besitzen, und vom Typ des Dokuments, das sie öffnen möchten.
  
Legen Sie diese Eigenschaften im **System.ExpandoProperties**-Eigenschaftensatz fest. 
  
|**Eigenschaft**|**Beschreibung**|**Typ**|**Beispiel**|
|:-----|:-----|:-----|:-----|
|**AppDisplayName** <br/> |Anbietername, der dem Benutzer angezeigt wird. Wird an mehreren Stellen in Office angezeigt, z. B. in der Liste der zuletzt verwendeten Dokumente.  <br/> |String  <br/> |Contoso  <br/> |
|**MicrosoftOfficeOwnershipType** <br/> |Geben Sie für die Lizenzierung an, ob der Dokumentspeicherort Persönlich/Verbraucher oder Geschäftlich/Unternehmen ist. Zulässige Werte sind 1 (persönlich) und 2 (geschäftlich). Wenn die Datei des Benutzers zum Beispiel in Contoso Business gespeichert ist, verwenden Sie den Wert "2" für "geschäftlich".  <br/> |Unit32  <br/> | 1 oder 2  <br/> Wenn die Datei des Benutzers zum Beispiel in Contoso Business gespeichert ist, sollte die Datei mit "2" für "geschäftlich" markiert werden.  <br/> |
|**MicrosoftOfficeTermsOfUse** <br/> |Rechtliche Hinweise, mit denen Sie erklären, dass die von Ihnen bereitgestellten Informationen nach unseren Nutzungsbedingungen korrekt sind. Dieser Text wird dem Benutzer nicht angezeigt. Es ist ein Vertrag zwischen Ihnen, dem Anwendungsanbieter, und Microsoft.  <br/> Sehen Sie sich das folgende Beispiel an.  <br/> | Zeichenfolge  <br/> | Ich stimme den Nutzungsbedingungen unter [https://go.microsoft.com/fwlink/p/?LinkId=528381](third-party-applications-integrating-with-office-mobile-products.md) zu. <br/> |
   
Das folgende Codebeispiel zeigt, wie Sie diese Eigenschaften festlegen können.
  
```cs
public static async Task SetExpandoProperties(StorageFile file,... other params ...) 
  { 
     var expandoProperties = new PropertySet(); 
     expandoProperties.Add("AppDisplayName", "Contoso",);  
     // String value. 
     expandoProperties.Add("MicrosoftOfficeOwnershipType", 1);  
     // Unit32 value - 1 (for personal), 2 (for business).  
     expandoProperties.Add("MicrosoftOfficeTermsOfUse", "I agree to the terms located at https://go.microsoft.com/fwlink/p/?LinkId=528381");   
    // String value. 
          
       var fileProperties = new PropertySet(); 
       fileProperties.Add("System.ExpandoProperties", expandoProperties); 
       await file.Properties.SavePropertiesAsync(fileProperties); 
  } 

```

## <a name="cached-file-updater-contracts"></a>Contracts für die Aktualisierung zwischengespeicherter Dateien

Wenn Ihre universelle App an Contracts für die Aktualisierung zwischengespeicherter Dateien beteiligt ist, wird sie benachrichtigt, wenn eine andere universelle App (z. B. Office) Änderungen an der Datei vornimmt. Informationen dazu, wie dies in Windows funktioniert, finden Sie unter [CachedFileUpdater-Klasse](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx).
  
Office verwendet die Option **AllowOnlyReaders** zum Öffnen der Dateien mit Lese-/Schreibzugriff, die Ihre universelle App über die Dateiauswahlverträge bietet. Das bedeutet, dass die Datei nicht von einer anderen App, auch nicht Ihrer eigenen, verschoben, gelöscht, umbenannt oder beschrieben werden kann, während sie in Office geöffnet ist. Office speichert die Datei automatisch, legt aber "CachedFileManager.DeferUpdates" fest, um die Aktivierung der App zu verhindern, bis Office das Dokument schließt oder Office von Windows angehalten wird (wenn der Benutzer zu einer anderen App wechselt). Wenn Office die Datei schließt, kann Ihre App in die Datei schreiben. 
  
Ihre App muss die gesamte Kommunikation mit Ihrem Dienst, z. B. Download, Aktualisierung und Upload, verarbeiten.
  
In den folgenden Tabellen sind die Parameter aufgelistet, die zum Verarbeiten von Interaktionen zwischen der App und Office festzulegen sind.
  
|**Parameter**|**Beschreibung**|
|:-----|:-----|
|[ReadActivationMode](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.readactivationmode.aspx) <br/> |Legen Sie **BeforeAccess** fest, damit Ihre App die Datei aktualisieren kann, bevor sie sie an Office sendet.  <br/> |
|[WriteActivationMode](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.writeactivationmode.aspx) <br/> |Legen Sie **ReadOnly** fest, um Schreibschutz für die Datei anzugeben. Legen Sie **AfterWrite** fest, um sicherzustellen, dass Ihre App durch den CacheFileUpdater ausgelöst wird, wenn Office die Bearbeitung der Datei abgeschlossen hat.  <br/><br/>**HINWEIS**: Wenn Sie **AfterWrite** nicht festlegen, wird Ihre App nicht benachrichtigt, die Änderungen hochzuladen. Änderungen des Benutzers erfolgen dann nur lokal.           |
|[CachedFileOptions.RequireUpdateOnAccess](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileoptions.aspx) <br/> |Legen Sie diese Eigenschaft fest, um sicherzustellen, dass Ihre App die Datei aktualisieren kann, wenn ein Benutzer über die Liste der zuletzt verwendeten Dokumente darauf zugreift.  <br/> |
   
## <a name="invoking-office-from-your-app"></a>Aufrufen von Office aus Ihrer App

When a user opens an Office document from your app, the document can open in Excel Mobile, PowerPoint Mobile, and Word Mobile. For example, when a user selects a \*.docx file in your app, Word Mobile launches with the \*.docx file opened. The Office app that opens is based on which app the user associated with the file type.
  
Zum Öffnen einer Datei aus Ihrer App in Office empfehlen wir die Verwendung von **LaunchFileAsync()**. Es wird nicht empfohlen, die Datei mit **LaunchUriAsync()** zu starten, da dann die für das URI-Schema registrierte Anwendung (der Browser) anstelle von Office gestartet wird. Zwar kann **LaunchUriAsync()** mit der Option **LauncherOptions.ContentType()** Office aufrufen, in diesem Fall wird aber die geöffnete Datei als temporär markiert und ist in Office schreibgeschützt. 
  
Weitere Informationen finden Sie unter [Launcher-Klasse](https://msdn.microsoft.com/library/windows/apps/windows.system.launcher.aspx).
  
## <a name="temporary-and-read-only-files"></a>Temporäre und schreibgeschützte Dateien

Legen Sie das **FILE_ATTRIBUTE_TEMPORARY**-Attribut für temporäre Dateien und das **FILE_ATTRIBUTE_READONLY**-Attribut für schreibgeschützte Dateien in Ihrer App fest. 
  
Dateien, deren Attribute **FILE_ATTRIBUTE_TEMPORARY** oder **FILE_ATTRIBUTE_READONLY** festgelegt sind, werden schreibgeschützt in Office geöffnet. **FILE_ATTRIBUTE_TEMPORARY** verhindert außerdem, dass die Datei in der Liste der zuletzt verwendeten Dokumente aufgeführt wird. 
  
Weitere Informationen zu Dateiattributen finden Sie unter [SetFileAttributes-Funktion](https://msdn.microsoft.com/library/windows/desktop/aa365535%28v=vs.85%29.aspx).
  
## <a name="other-best-practices"></a>Andere bewährte Methoden

Um die Dateikonsistenz zu optimieren, z. B. beim Auftreten von widersprüchlichen Änderungen oder Fehlern, sollten Sie die folgenden bewährten Methoden anwenden:
  
- Verhindern Sie Speicherkonflikte.
    
  - Unterbrechen Sie Uploads, wenn Serverkonflikte auftreten, um Verzweigungen zu vermeiden (Verzweigung nur wenn Office keine beschreibbare Datei mehr geöffnet hat). Wenn eine Datei von Ihrer App aus in Office geöffnet wurde, wird Ihre App in der Regel erst aktiviert, wenn Office geschlossen oder von Windows angehalten wird.
    
  - Wenn Sie eine Benutzeroberfläche zum Behandeln von Konflikten benötigen, implementieren Sie Toastbenachrichtigungen. Die vollständige Benutzeroberfläche ist nicht verfügbar, wenn Office angehalten wird.
    
- Behandeln Sie Fehler.
    
  - Wenn eine Sperre freigegeben wird, benachrichtigen Sie die Benutzer über den Konflikt, und geben Sie einen Pfad an, um ihn in Ihrer App zu beheben.
    
## <a name="see-also"></a>Siehe auch

- [Integration in Office](integrate-with-office.md)   
- [Integration in Office von Win32-Synchronisierungsclients aus](integrate-with-office-from-win32-sync-clients.md)
    

