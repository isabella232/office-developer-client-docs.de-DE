---
title: Erstellen von InfoPath-Formularvorlagen, die von InfoPath Forms Services unterstützt werden
manager: soliver
ms.date: 03/20/2015
ms.audience: Developer
keywords:
- browserkompatible Formularvorlagen [InfoPath 2007], Formulare [InfoPath 2007], browserkompatible, browserkompatible Formulare [InfoPath 2007], Formularvorlagen [InfoPath 2007], Browser kompatibel, InfoPath 2007, browserkompatible Formulare, Geschäftslogik InfoPath Forms Services, InfoPath Forms Services, Formulare erstellen, InfoPath Forms Services, unterstützte Objektmodellelemente, InfoPath Forms Services, unterstützte Klassen und Mitglieder
localization_priority: Normal
ms.assetid: 7bd4fbbb-49c6-46a1-9584-895e5aa9a772
description: Browser kompatible Formulare, die für Microsoft SharePoint Server 2013 mit InfoPath Forms Services bereitgestellt werden, unterstützen Features und Steuerelemente, die die Mehrzahl der InfoPath-Formulare verwenden. Browserkompatible Formulare, die von InfoPath Forms Services bereitgestellt werden, unterstützen jedoch nicht alle InfoPath-Features. Einige Features und Steuerelemente werden nicht auf dem Server implementiert. Für andere Features gibt es keine sinnvolle Darstellung auf dem Server.
ms.openlocfilehash: e2db35dc535af58b5f5116448f346cd7a527b681
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437105"
---
# <a name="creating-infopath-form-templates-that-work-with-infopath-forms-services"></a>Erstellen von InfoPath-Formularvorlagen, die von InfoPath Forms Services unterstützt werden

Browser kompatible Formulare, die für Microsoft SharePoint Server 2013 mit InfoPath Forms Services bereitgestellt werden, unterstützen Features und Steuerelemente, die die Mehrzahl der InfoPath-Formulare verwenden. Browserkompatible Formulare, die von InfoPath Forms Services bereitgestellt werden, unterstützen jedoch nicht alle InfoPath-Features. Einige Features und Steuerelemente werden nicht auf dem Server implementiert. Für andere Features gibt es keine sinnvolle Darstellung auf dem Server.
  
In den folgenden Abschnitten wird angegeben, welche Features in browserkompatiblen Formularen unterstützt werden, welche Features in browserkompatiblen Formularen nicht verwendet werden können und welche Features für browserkompatible Formulare angegeben werden können, aber in Webbrowsern nicht ausgeführt werden können.
  
## <a name="features-supported-by-both-infopath-and-infopath-forms-services"></a>Von InfoPath und InfoPath Forms Services unterstützte Features

In den folgenden Abschnitten sind die Features aufgeführt, die von browserkompatiblen Formularvorlagen unterstützt werden, die für InfoPath Forms Services bereitgestellt werden und sowohl in InfoPath als auch im Browser geöffnet werden können.
  
### <a name="controls"></a>Steuerelemente

Die folgenden Steuerelemente werden in Formularvorlagen unterstützt, die sowohl in InfoPath als auch im Browser geöffnet werden können.
  
- **Textfeld**
    
- **Feld für Rich-Text** (nur in Microsoft Internet Explorer bearbeitbar) 
    
- **Dropdown-Listenfeld**
    
- **Listenfeld**
    
- **Datumsauswahl** (wird in anderen Browsern als Internet Explorer als Textfeld gerendert) 
    
- **Kontrollkästchen**
    
- **Optionsfeld**
    
- **Button**
    
- **Section**
    
- **Optionaler Abschnitt**
    
- **Wiederholter Abschnitt**
    
- **Wiederholte Tabelle**
    
- **Dateianlage**
    
- **Hyperlink**
    
- **Ausdrucksfeld**
    
- **Kombinationsfeld**
    
- **Listenfeld für Mehrfachauswahl**
    
- **Aufzählung**
    
- **Nummerierte Liste**
    
- **Einfache Liste**
    
- **Picture**
    
- **Auswahlgruppe**
    
- **Auswahlabschnitt**
    
- **Personen-/Gruppenauswahl**
    
- **Auswahltool für externe Elemente**
    
- **Schaltfläche "Bild"**
    
- **Berechneter Wert**
    
### <a name="declarative-features"></a>Deklarative Features

Die folgenden deklarativen Features können sowohl in InfoPath als auch im Browser ausgeführt werden:
  
- Regeln
    
- Berechnungen
    
- Überprüfung
    
> [!NOTE]
> Einfache Regeln, Berechnungen und Datenüberprüfungen sind aktiviert und werden im Browser mithilfe von JScript ausgeführt. Komplexe Regeln, Berechnungen und Datenüberprüfungen erfordern ein Postback, um diese Vorgänge auf dem Server auszuführen. 
  
### <a name="code"></a>Code

Der Geschäftslogikcode muss auf dem InfoPath-Objektmodell verwalteter Code basieren, das vom [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellt wird. Geschäftslogikcode, der auf dem Server ausgeführt wird, unterliegt den folgenden Einschränkungen: 
  
- Da jede Serveranforderung möglicherweise von einem anderen Front-End verarbeitet wird und InfoPath Forms Services nur eine Instanz der Geschäftslogik lädt, können Programmierer nicht auf Daten, die in globalen oder statischen Variablen gespeichert sind, zurückgreifen. Um dies zu ermöglichen, muss die Geschäftslogik den Status in einem Eigenschaftenbehälter speichern, auf den von der [FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx) -Eigenschaft bereitgestellt wird. 
    
- Ein Subset der Member des **Microsoft.Office.InfoPath**-Namespace stellt Features wie RIM (Information Rights Management, Verwaltung von Informationsrechten) bereit, die auf dem Server nicht unterstützt werden. Weitere Informationen zu den nicht unterstützten Objektmodellmembern finden Sie in den Abschnitten "Objektmodellmember, die in InfoPath und InfoPath Forms Services ausgeführt werden können" und "Objektmodellmember, die nur in InfoPath ausgeführt werden können" weiter unten in diesem Thema. 
    
- Die in VBScript, JScript geschriebene Geschäftslogik und das von Mitgliedern des [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace bereitgestellte InfoPath 2003-kompatible Objektmodell werden auf dem Server nicht unterstützt. 
    
## <a name="features-not-supported-by-infopath-forms-services"></a>Features, die von InfoPath Forms Services nicht unterstützt werden

In den folgenden Abschnitten sind die Features aufgeführt, die von browserkompatiblen Formularvorlagen, die für InfoPath Forms Services bereitgestellt werden, nicht unterstützt werden, die sowohl in InfoPath als auch im Browser geöffnet werden können.
  
Wenn Sie das Feature **Design Checker** im InfoPath-Entwurfsmodus verwenden, um die Kompatibilität mit InfoPath Forms Services zu bestätigen, werden nicht unterstützte Features entweder zu Fehlern oder Nachrichten. Fehler verursachende Features verhindern, dass die Formularvorlage als browserfähiges Formular veröffentlicht wird. Features, die Nachrichten erzeugen, sind zulässig, aber diese Funktion wird nicht ausgeführt, wenn das Formular in einem Browser geöffnet wird. 
  
### <a name="controls"></a>Steuerelemente

Die folgenden Steuerelemente und Steuerelementfeatures werden in Formularvorlagen nicht unterstützt, die in InfoPath und im Browser geöffnet werden können.
  
- Filter für wiederholte Steuerelemente
    
- **Master/Detail**
    
- **Vertikales Etikett**
    
- **Horizontale wiederholte Tabelle**
    
- **Freihandzeichnung**
    
- **Wiederholter rekursiver Abschnitt**
    
### <a name="other-features-that-are-not-supported-or-not-fully-supported-by-infopath-forms-services"></a>Andere Features, die von InfoPath Forms Services nicht oder nur teilweise unterstützt werden

Andere Features, die in InfoPath Forms Services nicht unterstützt werden:
  
- ActiveX-Steuerelemente
    
- HTML-Aufgabenbereiche
    
- Platzhaltertext in Steuerelementen, z. B. "Klicken Sie hier, um Text einzugeben" (im Browser wird kein Text angezeigt)
    
- Für Datenbankdatenverbindungen besteht schreibgeschützter Zugriff auf SQL-Serverdatenbanken
    
- Benutzerrollen
    
- Digitale Signaturerweiterbarkeit durch das Objektmodell. Digitales Signieren auf dem Server wird durch ein ActiveX-Steuerelement unterstützt, das nur in Microsoft Internet Explorer ausgeführt wird.
    
- Integration von HWS (Human Workflow Services). HWS wird von BizTalk Server abgelehnt.
    
- Außerkraftsetzungen von XML-Schemafehlermeldungen. Dies ist ein selten verwendetes Feature, mit dessen Hilfe der Formularentwickler eine andere Meldung als die Meldung von MSXML oder **System.Xml** bereitstellen kann, wenn ein Dokument nicht überprüft werden kann (in der Regel aufgrund eines Typkonflikts). Dieses Feature wird in der Entwurfsbenutzeroberfläche nicht unterstützt und erfordert eine manuelle Bearbeitung der Formulardefinitionsdatei (XSF). 
    
### <a name="features-with-no-direct-parallel-on-the-infopath-forms-services"></a>Features ohne direkte Parallele in InfoPath Forms Services

Andere Features, die in InfoPath Forms Services nicht unterstützt werden:
  
- Popup-Dialogfelder bei der Validierung ohne Modus
    
- Outlook-Integration
    
- COM-Add-Ins
    
- Formulare zusammenführen
    
- Automatisches Speichern, Absturzermittlung und Wiederherstellung
    
- E-Mail-Umschlag
    
- Exportieren nach Excel
    
- Tablett-/Freihandfeatures, einschließlich des Steuerelements **Freihandzeichnung** 
    
- Rückgängig / Wiederholen
    
- RIM (Information Rights Management, Verwaltung von Informationsrechten)
    
- Modale Dialogfelder aus Geschäftslogik
    
- XSLT-Erweiterbarkeit (**xd:preserve**-Blöcke) 
    
- Externe Automatisierung
    
- Zwischenspeicherung von Offlineabfragen
    
- Rechtschreibprüfung
    
- Eingeschränkter Sicherheitsmodus
    
> [!NOTE]
> Von diesen Features werden beim Verwenden des Features **Designdetektiv** im InfoPath-Entwurfsmodus keine Fehler oder Meldungen verursacht. 
  
## <a name="object-model-members-that-work-in-both-infopath-and-infopath-forms-services"></a>Objektmodellmember, die in InfoPath und InfoPath Forms Services ausgeführt werden können

InfoPath bietet ein neues Objektmodell mit verwaltetem Code, das über eine Hauptgruppe von Funktionalitäten zum Erstellen von benutzerdefinierter Geschäftslogik in Formularvorlagen verfügt. Bei der Bereitstellung in SharePoint Server 2010 mit InfoPath Forms Services wird die mit diesem neuen Objektmodell erstellte Geschäftslogik sowohl in einem Webbrowser als auch in InfoPath ausgeführt. Optional können Sie Geschäftslogik schreiben, die eine zusätzliche Funktionalität in diesem Objektmodell verwendet, die nur in Formularvorlagen ausgeführt wird, die zur Bearbeitung in InfoPath geöffnet sind.
  
Wenn Sie eine Geschäftslogik schreiben möchten, die ausgeführt wird, wenn ein Formular sowohl in einem Webbrowser als auch in InfoPath geöffnet wird, aktivieren Sie beim Erstellen einer neuen Formularvorlage das Kontrollkästchen **Nur browserkompatible Features aktivieren** im Dialogfeld **Formularvorlage entwerfen** . Wenn Sie eine Geschäftslogik schreiben möchten, die beim Öffnen in InfoPath zusätzliche Funktionen verwenden kann, deaktivieren Sie das Kontrollkästchen **Nur browserkompatible Features aktivieren** , wenn Sie eine neue Formularvorlage erstellen. Sie können diese Einstellung auch nach dem Erstellen einer Formularvorlage ändern, indem Sie im Aufgabenbereich **Designdetektiv** auf **Kompatibilitätseinstellungen ändern** klicken und dann **eine Formularvorlage, die in einem Browser oder InfoPath geöffnet werden kann, aktivieren oder deaktivieren. **Kontrollkästchen. Wenn Sie eine browserkompatible Formularvorlage erstellen, zeigt der Compiler eine Fehlermeldung an, wenn Sie Klassen oder Member verwendet haben, die nicht mit InfoPath Forms Services kompatibel sind. 
  
> [!NOTE]
> Nachdem Sie eine browserfähige Formularvorlage mit verwaltetem Code zu SharePoint Server 2010 mit InfoPath Forms Services oder an einem freigegebenen Speicherort veröffentlicht haben, muss die Formularvorlage hochgeladen und von einem Server Administrator genehmigt werden, bevor Sie ausgeführt werden kann. 
  
Die folgenden Klassen und Member des InfoPath-Objektmodells mit verwaltetem Code, das vom [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellt wird, werden in InfoPath und InfoPath Forms Services unterstützt. 
  
|**Übergeordnete Klasse**|**Elemente**|
|:-----|:-----|
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) <br/> |
||[Befehl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Command.aspx) <br/> |
||[Connection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) <br/> |
||[Timeout](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Timeout.aspx) <br/> |
||[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) <br/> |
||[Befehl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.Command.aspx) <br/> |
||[Connection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.Connection.aspx) <br/> |
||[Timeout](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.Timeout.aspx) <br/> |
|[Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) <br/> |[Umgebung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) <br/> |
||[Benutzer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.User.aspx) <br/> |
|[Button Event](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) <br/> |[Geklickt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) <br/> |
|[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |[ControlId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.ControlId.aspx) <br/> |
||[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) <br/> |
|[ControlEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ControlEvents.aspx) <br/> |[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ControlEvents.Item.aspx) <br/> |
|[DataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Name.aspx) <br/> |
|[DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.GetEnumerator.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.Item.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.Item.aspx) <br/> |
|[DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) <br/> |
||[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx) <br/> |
||[QueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx) <br/> |
||[ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx) <br/> |
||[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) <br/> |
|[DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx) <br/> |
|[EmailAttachmentType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.aspx) <br/> |[None](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.None.aspx) <br/> |
||[XML](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.Xml.aspx) <br/> |
||[XmlXsn](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailAttachmentType.XmlXsn.aspx) <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |[AttachmentFileName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.AttachmentFileName.aspx) <br/> |
||[Bcc](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Bcc.aspx) <br/> |
||[CC](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.CC.aspx) <br/> |
||[EmailAttachmentType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.EmailAttachmentType.aspx) <br/> |
||[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) <br/> |
||[Einführung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Introduction.aspx) <br/> |
||[Betreff](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Subject.aspx) <br/> |
||[Ziel](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.To.aspx) <br/> |
|[Umgebung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) <br/> |[IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) <br/> |
||[IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) <br/> |
|[Event Manager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.aspx) <br/> |[ControlEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.ControlEvents.aspx) <br/> |
||[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.FormEvents.aspx) <br/> |
||[XmlEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EventManager.XmlEvents.aspx) <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) <br/> |
||[FileLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.FileLocation.aspx) <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) <br/> |
||[Filename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Filename.aspx) <br/> |
||[FolderUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.FolderUrl.aspx) <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |[DetailedMessage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx) <br/> |
||[FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx) <br/> |
||[Nachricht](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Name.aspx) <br/> |
||[Website](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
||[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx) <br/> |
||[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) <br/> |
||[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) <br/> |
||[DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetEnumerator.aspx) <br/> |
||[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) <br/> |
||[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx) <br/> |
|[FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.aspx) <br/> |[Schema Validation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.SchemaValidation.aspx) <br/> |
||[SystemGenerated](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.SystemGenerated.aspx) <br/> |
||[UserDefined](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorType.UserDefined.aspx) <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[Laden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) <br/> |
||[Senden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) <br/> |
||[VersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.VersionUpgrade.aspx) <br/> |
||[ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) <br/> |
|[Form Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) <br/> |
||[OpenFileFromPackage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.OpenFileFromPackage.aspx) <br/> |
||[Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx) <br/> |
||[Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx) <br/> |
|[LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.CancelableArgs.aspx) <br/> |
||[InputParameters](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.InputParameters.aspx) <br/> |
||[SetDefaultView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.SetDefaultView.aspx) <br/> |
||[SetDefaultView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.SetDefaultView.aspx) <br/> |
|[SharepointListQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) <br/> |
||[QueryThisFormOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.QueryThisFormOnly.aspx) <br/> |
||[SiteUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.SiteUrl.aspx) <br/> |
|[SubmitEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.CancelableArgs.aspx) <br/> |
|[Benutzer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) <br/> |[LoginName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.LoginName.aspx) <br/> |
||[UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) <br/> |
|[VersionUpgradeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.CancelableArgs.aspx) <br/> |
||[DocumentVersion](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.DocumentVersion.aspx) <br/> |
||[FormTemplateVersion](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.FormTemplateVersion.aspx) <br/> |
|[Ansicht](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) <br/> |
|[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) <br/> |[Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.Caption.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.Name.aspx) <br/> |
|[ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Count.aspx) <br/> |
||[Default](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Default.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.GetEnumerator.aspx) <br/> |
||[Ersten](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Item.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Item.aspx) <br/> |
||[SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) <br/> |
||[SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) <br/> |
||[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) <br/> |
||[ServiceUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.ServiceUrl.aspx) <br/> |
||[SoapAction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.SoapAction.aspx) <br/> |
||[Timeout](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Timeout.aspx) <br/> |
||[WsdlUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.WsdlUrl.aspx) <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Geändert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) <br/> |
||[RaiseUndoRedoForChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.RaiseUndoRedoForChanged.aspx) <br/> |
||[Überprüfen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) <br/> |
|[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |[Match](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Match.aspx) <br/> |
||[NewValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.NewValue.aspx) <br/> |
||[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) <br/> |
||[OldValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldValue.aspx) <br/> |
||[Vorgang](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Operation.aspx) <br/> |
||[Website](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) <br/> |
||[UndoRedo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.UndoRedo.aspx) <br/> |
|[XmlEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvents.aspx) <br/> |[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvents.Item.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvents.Item.aspx) <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |[CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) <br/> |
||[DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) <br/> |
||[DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) <br/> |
||[Fehler](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) <br/> |
||[FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx) <br/> |
||[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) <br/> |
||[NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) <br/> |
||[New](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx) <br/> |
||[NotifyHost](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NotifyHost.aspx) <br/> |
||[QueryDataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx) <br/> |
||[ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx) <br/> |
||[Angemeldeten](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) <br/> |
||[Senden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) <br/> |
||[Vorlage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) <br/> |
||[Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx) <br/> |
||[ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) <br/> |
||[XmlLang](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx) <br/> |
|[XmlFormCancelEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.aspx) <br/> |[Nachricht](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.Message.aspx) <br/> |
||[MessageDetails](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.MessageDetails.aspx) <br/> |
|[XmlOperation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.aspx) <br/> |[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.Delete.aspx) <br/> |
||[Insert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.Insert.aspx) <br/> |
||[None](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.None.aspx) <br/> |
||[ValueChange](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.ValueChange.aspx) <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
||[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
||[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
|[XPathTypedValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.aspx) <br/> |[Evaluate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.Evaluate.aspx) <br/> |
||[SetStringValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.SetStringValue.aspx) <br/> |
||[ToString](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.ToString.aspx) <br/> |
||[XPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XPathTypedValue.XPath.aspx) <br/> |
   
## <a name="object-model-members-that-work-only-in-infopath"></a>Objektmodellmember, die nur in InfoPath ausgeführt werden können

Die folgenden Klassen und Member des InfoPath-Objektmodells mit verwaltetem Code, das vom [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellt wird, werden nur in InfoPath unterstützt. 
  
> [!NOTE]
> Diese Objektmodellelemente können im Code einer browserfähigen Formularvorlage verwendet werden, wenn Sie eine bedingte Logik schreiben, die bestimmt, ob das Formular im Browser oder in InfoPath geöffnet wird. Weitere Informationen finden Sie unter [Write Conditional Logic, die die Laufzeitumgebung bestimmt](how-to-write-conditional-logic-that-determines-the-run-time-environment.md). 
  
|**Übergeordnete Klasse**|**Elemente**|
|:-----|:-----|
|[ActionType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.aspx) <br/> |[Copy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Copy.aspx) <br/> |
||[Cut](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Cut.aspx) <br/> |
||[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Delete.aspx) <br/> |
||[Paste](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.Paste.aspx) <br/> |
||[XCollectionInsert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionInsert.aspx) <br/> |
||[XCollectionInsertAfter](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionInsertAfter.aspx) <br/> |
||[XCollectionInsertBefore](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionInsertBefore.aspx) <br/> |
||[XCollectionRefreshFilter](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionRefreshFilter.aspx) <br/> |
||[XCollectionRemove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionRemove.aspx) <br/> |
||[XCollectionRemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XCollectionRemoveAll.aspx) <br/> |
||[XFileAttachmentAttach](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentAttach.aspx) <br/> |
||[XFileAttachmentOpen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentOpen.aspx) <br/> |
||[XFileAttachmentRemove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentRemove.aspx) <br/> |
||[XFileAttachmentSaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XFileAttachmentSaveAs.aspx) <br/> |
||[XOptionalInsert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XOptionalInsert.aspx) <br/> |
||[XOptionalRemove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XOptionalRemove.aspx) <br/> |
||[XReplaceReplace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ActionType.XReplaceReplace.aspx) <br/> |
|[Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) <br/> |[ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) <br/> |
||[Läuft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.CacheFormTemplate.aspx) <br/> |
||[ComAddIns](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ComAddIns.aspx) <br/> |
||[GetFormTemplateLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.GetFormTemplateLocation.aspx) <br/> |
||[IsDestinationReachable](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.IsDestinationReachable.aspx) <br/> |
||[LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) <br/> |
||[MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) <br/> |
||[Quit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Quit.aspx) <br/> |
||[Quit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Quit.aspx) <br/> |
||[RegisterFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.RegisterFormTemplate.aspx) <br/> |
||[RegisterFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.RegisterFormTemplate.aspx) <br/> |
||[UnregisterFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.UnregisterFormTemplate.aspx) <br/> |
||[UsableHeight](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.UsableHeight.aspx) <br/> |
||[UsableWidth](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.UsableWidth.aspx) <br/> |
||[Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) <br/> |
||[Windows](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) <br/> |
||[XmlForms](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) <br/> |
|[Certificate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |[ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.ExpirationDate.aspx) <br/> |
||[IssuedBy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.IssuedBy.aspx) <br/> |
||[IssuedTo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.IssuedTo.aspx) <br/> |
||[Status](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.Status.aspx) <br/> |
|[CertificateStatus](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.aspx) <br/> |[Fehler](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Error.aspx) <br/> |
||[Abgelaufen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Expired.aspx) <br/> |
||[NotTrusted](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.NotTrusted.aspx) <br/> |
||[Gesperrt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Revoked.aspx) <br/> |
||[Valid](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.CertificateStatus.Valid.aspx) <br/> |
|[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |[ChangeType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.ChangeType.aspx) <br/> |
||[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) <br/> |
||[UndoRedo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.UndoRedo.aspx) <br/> |
|[ErrorMode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ErrorMode.aspx) <br/> |[Modal](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ErrorMode.Modal.aspx) <br/> |
||[MODELESS](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ErrorMode.Modeless.aspx) <br/> |
|[ExportFormat](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.aspx) <br/> |[MHT](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.Mht.aspx) <br/> |
||[Pdf](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.Pdf.aspx) <br/> |
||[XPS](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ExportFormat.Xps.aspx) <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |[ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx) <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) <br/> |
||[Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) <br/> |
||[Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) <br/> |
||[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |
|[Form Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |[CacheId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx) <br/> |
|[HtmlTaskPane](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.aspx) <br/> |[HtmlDocument](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.HtmlDocument.aspx) <br/> |
||[HtmlWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.HtmlWindow.aspx) <br/> |
||[Navigieren Sie](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.HtmlTaskPane.Navigate.aspx) <br/> |
|[MachineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.aspx) <br/> |[IEInOfflineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.IEInOfflineState.aspx) <br/> |
||[Offline](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.Offline.aspx) <br/> |
||[Online](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MachineState.Online.aspx) <br/> |
|[MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx) <br/> |[Available](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Available.aspx) <br/> |
||[Bcc](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Bcc.aspx) <br/> |
||[CC](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.CC.aspx) <br/> |
||[EmailAttachmentType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.EmailAttachmentType.aspx) <br/> |
||[Einführung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Introduction.aspx) <br/> |
||[Betreff](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Subject.aspx) <br/> |
||[Ziel](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.To.aspx) <br/> |
||[Visible](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.Visible.aspx) <br/> |
|[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.CancelableArgs.aspx) <br/> |
||[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Count.aspx) <br/> |
||[Index](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Index.aspx) <br/> |
||[Rollback](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Rollback.aspx) <br/> |
||[XML](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) <br/> |
|[Berechtigung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) <br/> |[ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) <br/> |
||[DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) <br/> |
||[Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) <br/> |
||[PermissionFromPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PermissionFromPolicy.aspx) <br/> |
||[PolicyDescription](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyDescription.aspx) <br/> |
||[PolicyName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyName.aspx) <br/> |
||[RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) <br/> |
||[StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) <br/> |
||[UserPermissions](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.UserPermissions.aspx) <br/> |
|[PermissionType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.aspx) <br/> |[Ändern](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Change.aspx) <br/> |
||[Bearbeiten](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Edit.aspx) <br/> |
||[Extrahieren](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Extract.aspx) <br/> |
||[Vollzugriff](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.FullControl.aspx) <br/> |
||[ObjectModel](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.ObjectModel.aspx) <br/> |
||[Print](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Print.aspx) <br/> |
||[Lesen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Read.aspx) <br/> |
||[Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.Save.aspx) <br/> |
||[Ansicht](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.View.aspx) <br/> |
|[SaveEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.CancelableArgs.aspx) <br/> |
||[CloseIfSaveCancelled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveCancelEventArgs.CloseIfSaveCancelled.aspx) <br/> |
||[Filename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.Filename.aspx) <br/> |
||[IsSaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.IsSaveAs.aspx) <br/> |
||[PerformSaveOperation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.PerformSaveOperation.aspx) <br/> |
|[Signatur](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |[Certificate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Certificate.aspx) <br/> |
||[Kommentar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Comment.aspx) <br/> |
||[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) <br/> |
||[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) <br/> |
||[Status](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Status.aspx) <br/> |
|[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.Count.aspx) <br/> |
||[CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.GetEnumerator.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.Item.aspx) <br/> |
|[SignatureRelation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.aspx) <br/> |[Cosign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.Cosign.aspx) <br/> |
||[CounterSign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.CounterSign.aspx) <br/> |
||[Single](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureRelation.Single.aspx) <br/> |
|[SignatureStatus](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.aspx) <br/> |[Fehler](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Error.aspx) <br/> |
||[Invalid](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Invalid.aspx) <br/> |
||[Unsupported](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Unsupported.aspx) <br/> |
||[Valid](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureStatus.Valid.aspx) <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |[Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Caption.aspx) <br/> |
||[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Name.aspx) <br/> |
||[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) <br/> |
||[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) <br/> |
||[SignatureRelation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureRelation.aspx) <br/> |
||[Signaturen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) <br/> |
||[XPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.XPath.aspx) <br/> |
|[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.GetEnumerator.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.Item.aspx) <br/> |
||[ShowSignatureDialog](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.ShowSignatureDialog.aspx) <br/> |
|[SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) <br/> |[SignatureWizard](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |
||[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |
|[TaskPane](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPane.aspx) <br/> |[TaskPaneType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPane.TaskPaneType.aspx) <br/> |
||[Visible](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPane.Visible.aspx) <br/> |
|[TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.GetEnumerator.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.Item.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.Item.aspx) <br/> |
|[TaskPaneType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.aspx) <br/> |[BulletsNumbering](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.BulletsNumbering.aspx) <br/> |
||[ClipArt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.ClipArt.aspx) <br/> |
||[Suchen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Find.aspx) <br/> |
||[Formatierung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Formatting.aspx) <br/> |
||[HTML](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Html.aspx) <br/> |
||[ParagraphFormatting](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.ParagraphFormatting.aspx) <br/> |
||[Replace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Replace.aspx) <br/> |
||[Rechtschreib](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneType.Spelling.aspx) <br/> |
|[Benutzer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) <br/> |[IsUserMemberOf](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.IsUserMemberOf.aspx) <br/> |
|[UserPermission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.aspx) <br/> |[ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.ExpirationDate.aspx) <br/> |
||[Berechtigung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Permission.aspx) <br/> |
||[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Remove.aspx) <br/> |
||[UserId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.UserId.aspx) <br/> |
|[UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.aspx) <br/> |[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) <br/> |
||[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.GetEnumerator.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) <br/> |
||[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) <br/> |
||[RemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.RemoveAll.aspx) <br/> |
|[Ansicht](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) <br/> |
||[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) <br/> |
||[ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) <br/> |
||[ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) <br/> |
||[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) <br/> |
||[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) <br/> |
||[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) <br/> |
||[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) <br/> |
||[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) <br/> |
||[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) <br/> |
||[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) <br/> |
||[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) <br/> |
||[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) <br/> |
||[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) <br/> |
||[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) <br/> |
||[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) <br/> |
|[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) <br/> |[HideName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.HideName.aspx) <br/> |
|[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) <br/> |[Activate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx) <br/> |
||[Active](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx) <br/> |
||[Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx) <br/> |
||[Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx) <br/> |
||[Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx) <br/> |
||[CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) <br/> |
||[Height](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx) <br/> |
||[Left](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx) <br/> |
||[MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx) <br/> |
||[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx) <br/> |
||[Top](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx) <br/> |
||[Width](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx) <br/> |
||[WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx) <br/> |
||[WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx) <br/> |
||[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx) <br/> |
|[WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx) <br/> |
||[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.GetEnumerator.aspx) <br/> |
||[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx) <br/> |
|[WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx) <br/> |[Maximiert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.Maximized.aspx) <br/> |
||[Minimized](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.Minimized.aspx) <br/> |
||[Normal](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.Normal.aspx) <br/> |
|[WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) <br/> |[Designer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.Designer.aspx) <br/> |
||[Editor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.Editor.aspx) <br/> |
|[XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) <br/> |[CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.CancelableArgs.aspx) <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Ändern](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |[Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Close.aspx) <br/> |
||[Dirty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx) <br/> |
||[Extension](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx) <br/> |
||[GetWorkflowTasks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTasks.aspx) <br/> |
||[GetWorkflowTemplates](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTemplates.aspx) <br/> |
||[Host](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx) <br/> |
||[Gehostet](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx) <br/> |
||[HostName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx) <br/> |
||[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) <br/> |
||[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) <br/> |
||[Berechtigung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) <br/> |
||[Print](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) <br/> |
||[Print](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) <br/> |
||[Erholt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx) <br/> |
||[Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx) <br/> |
||[SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) <br/> |
||[SetSaveAsDialogFilename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogFilename.aspx) <br/> |
||[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogLocation.aspx) <br/> |
||[SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) <br/> |
||[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx) <br/> |
||[UserRole](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx) <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx) <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.GetEnumerator.aspx) <br/> |
||[Element](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx) <br/> |
||[New](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) <br/> |
||[New](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) <br/> |
||[Open](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) <br/> |
||[Open](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) <br/> |
|[XmlFormOpenMode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormOpenMode.aspx) <br/> |**XmlFormOpenMode. Default** <br/> |
||**XmlFormOpenMode. FailOnVersionMismatch** <br/> |
||**XmlFormOpenMode. FailOnVersionOlder** <br/> |
||**XmlFormOpenMode. IgnoreDataConnectionsFailure** <br/> |
||**XmlFormOpenMode. PromptIfSigned** <br/> |
||**XmlFormOpenMode. ReadOnly** <br/> |
||**XmlFormOpenMode. TransformEvenIfSigned** <br/> |
||**XmlFormOpenMode. UseExistingVersion** <br/> |
||**XmlFormOpenMode. UseFileConverter** <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) <br/> |
   

