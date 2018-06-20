---
title: Arbeiten Sie mit digitalen Signaturen mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- digitale Signaturen [Infopath 2007], Infopath 2003-kompatible Formularvorlagen, InfoPath 2003-kompatible Formularvorlagen, digitale Signaturen
localization_priority: Normal
ms.assetid: d6318238-fd45-4854-a3c9-c27c5685bd6b
description: Das InfoPath 2003-kompatible Objektmodell bietet Features zum programmgesteuerten Verwenden von digitalen Signaturen.
ms.openlocfilehash: ae9934e36766b7e783d1404a12a49e9b0b08543a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790757"
---
# <a name="work-with-digital-signatures-using-the-infopath-2003-object-model"></a>Arbeiten Sie mit digitalen Signaturen mithilfe des InfoPath 2003-Objektmodells

Das InfoPath 2003-kompatible Objektmodell bietet Features zum programmgesteuerten Verwenden von digitalen Signaturen.
  
## <a name="digital-signature-features"></a>Features für digitale Signaturen

Mithilfe der Features für digitale Signaturen in InfoPath können Sie Folgendes ausführen:  
  
- Ermöglichen von Signaturen für das gesamte Formular oder für bestimmte Gruppen von Daten im Formular, die getrennt signiert werden können.
    
- Angeben bei jeder signierbaren Datengruppe, ob einzelne oder mehrere Signaturen zulässig sind und in welcher Beziehung diese zueinander stehen sollen. So können Sie beispielsweise angeben, ob es sich um parallele gemeinsame Signaturen handelt oder ob alle früheren Signaturen durch jede neue Signatur gegengezeichnet werden.
    
- Angeben einer Meldung, die angezeigt werden soll, wenn Benutzer das Formular signieren.
    
- Einfügen und Anzeigen einer Signatur im Dokument.  
    
- Überprüfbar Nichtabstreitbarkeit Informationen anzeigen, der jede Signatur, um eine höhere Sicherheit hinzugefügt wurde. Diese zusätzlichen Informationen, die eine Ansicht des Formulars enthält, wie es jeder signierenden Person vorgelegt wurde, ist Teil der Signatur und kann nicht entfernt werden, ohne dass die Signatur ungültig wird. Zu einem beliebigen Zeitpunkt können Sie diese Daten Denken Sie daran, indem Sie auf die Signatur im Formular, um das Dialogfeld **Digitale Signatur überprüfen** angezeigt werden soll. 
    
- Profitieren von einem umfangreicheren Objektmodell zum Arbeiten mit digitalen Signaturen. Fügen Sie dem Signaturblock in vollständig vertrauenswürdigen Formularen benutzerdefinierte Informationen zum Objektmodell für digitale Signaturen hinzu.  
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Übersicht über das Objektmodell für digitale Signaturen

### <a name="events"></a>Ereignisse

Das Objektmodell für digitale Signaturen stellt das folgende Ereignis bereit.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |Tritt ein, nachdem eine signierbare Datengruppe zum Signieren ausgewählt wurde.  <br/> Mithilfe dieses Ereignisses können Sie die in der digitalen Signatur gespeicherten Daten bearbeiten. So können Sie beispielsweise Daten eines vertrauenswürdigen Zeitstempelservers oder eine serverseitige Gegensignatur der Transaktion hinzufügen. Sie können mit diesem Ereignis auch Signaturen blockieren, wenn der aktuelle Benutzer kein Mitglied einer bestimmten Gruppe ist.  <br/> |
   
Das **OnSign** -Ereignis gibt einen Verweis auf das [SignEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) -Objekt, das die folgenden Eigenschaften bereitstellt. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.ReturnStatus.aspx) <br/> |Dient zum Abrufen oder Festlegen eines **booleschen** Werts, der den Rückgabestatus des **OnSign** -Ereignisses angibt.  <br/> |
|[SignedDataBlock-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.SignedDataBlock.aspx) <br/> |Ruft das signierte Datenblock das **OnSign** -Ereignis ausgelöst hat.  <br/> |
|[XDocument-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.XDocument.aspx) <br/> |Ruft einen Verweis auf das **XDocument** -Objekt, das dem **OnSign** -Ereignis zugeordnet.  <br/> |
   
### <a name="collections-and-objects"></a>Auflistungen und Objekte

Das Objektmodell für digitale Signaturen stellt die folgenden Auflistungen bereit.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[SignedDataBlocksCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlocksCollection.aspx) <br/> |Die Auflistung der Objekte [signeddatablockobject-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) in der Formularvorlage gemäß Definition in der Formulardefinitionsdatei (XSF).  <br/> Die **SignedDataBlocksCollection** -Auflistung implementiert Eigenschaften, die Zugriff auf das einem Formular zugeordnete **SignedDataBlockObjects** -Objekte verwendet werden können. Die **SignedDataBlocks** -Auflistung kann über die [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) -Eigenschaft des [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Objekts zugegriffen werden.  <br/> |
|[SignaturesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignaturesCollection.aspx) <br/> |Enthält eine Auflistung von [SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) -Objekten für jedes **signeddatablockobject-Objekt** im Formular.  <br/> Die **SignaturesCollection** -Auflistung implementiert Eigenschaften und eine Methode, die Zugriff auf ein Formular zugeordnete **SignatureObject** -Objekte und zum Erstellen einer Signatur verwendet werden kann. Es kann über das Objekt **signeddatablockobject-Objekt** zugegriffen werden.  <br/> Beachten Sie bei Verwendung die [Create](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) -Methode der **SignaturesCollection** -Auflistung Denken Sie daran, die die Signatur bis das [Zeichen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) nicht geschrieben werden-Methode für das **SignatureObject** -Objekt aufgerufen wird. Diese Methoden können nur aus einer voll vertrauenswürdigen Formularvorlage **OnSign** -Ereignishandler aufgerufen werden.  <br/> |
   
Das Objektmodell für digitale Signaturen stellt die folgenden Objekte bereit.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Signeddatablockobject-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) <br/> |Stellt einen Satz signierbarer Daten in einem Formular dar. Das **SignedDataBlock** -Objekt bietet eine Reihe von Eigenschaften und eine Methode, die für die programmgesteuerte Interaktion mit einem Satz signierbarer Daten verwendet werden können.  <br/> |
|[Signatureobject-Objekts](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) <br/> |Stellt eine digitale Signatur, die an ein Formular oder eine signierbare Datengruppe in einem Formular hinzugefügt wurde. Die **SignatureObject** -Auflistung implementiert Eigenschaften, die zum Abrufen von Informationen über die digitale Signatur und die [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) -Methode zum Schreiben des XML-Blocks mit digitalen Signaturen und dessen Wert kryptografischen Hash computing verwendet werden können.  <br/> |
|[CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) <br/> |Stellt das digitale X.509-Zertifikat dar, das zum Erstellen der Signatur verwendet wurde.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Programmgesteuertes Arbeiten mit digitalen Signaturen

Das InfoPath 2003-kompatible Objektmodell stellt Member für die programmgesteuerte Interaktion mit digitalen Signaturen bereit. So können insbesondere in vollständig vertrauenswürdigen Formularen benutzerdefinierte Informationen dem Signaturblock hinzugefügt werden, bevor ein Commit für ihn ausgeführt wird. Dies geschieht entsprechend dem folgenden Zeitplan:
  
1. Der Benutzer entscheidet, dass einem Formular eine digitale Signatur hinzugefügt werden soll.
    
2. Das erste Fenster des **Assistenten für digitale Signaturen** wird angezeigt. 
    
3. Für die ausgewählten Daten, die durch das Objekt **signeddatablockobject-Objekt** dargestellten das **OnSign** -Ereignis wird ausgelöst, und die **Sign** -Methode des **signeddatablockobject-Objekt** und die **Create** -Methode von der **SignaturesCollection** Auflistung ausgeführt werden. 
    
4. Alle optionalen benutzerdefinierten Aktionen werden ausgeführt.
    
5. Die **Sign** -Methode des **signatureobject-Objekts** die wird ausgeführt. 
    
6. Das zweite und dritte Fenster des Assistenten werden angezeigt, in denen ein Zertifikat zum Signieren ausgewählt und Kommentare eingegeben werden können.
    
7. Die nichtabstreitbarkeitsinformationen werden angezeigt (weiter unten im Dialogfeld **Digitale Signatur überprüfen** angezeigt werden können). 
    
8. Wenn die Schaltfläche **Signieren** geklickt wird, wird die Signatur Auflistung von Signaturen für das Formular hinzugefügt. 
    
Im folgenden Beispiel wird das Dialogfeld **Signieren** und Countersigns die Signatur mit einem Zeitstempelwert von einem vertrauenswürdigen Zeitstempeldienst abgerufen. 
  
```cs
[InfoPathEventHandler(EventType=InfoPathEventType.OnSign)]
public void OnSign(SignEvent e)
{
    Signature signature = e.SignedDataBlock.Signatures.Create();
    // Invoke the Sign dialog box to sign the data block.
    signature.Sign();
    // Countersign the signature with a trusted timestamp
    // Get the XML node storing the signature block
    IXMLDOMNode oNodeSig = signature.SignatureBlockXmlNode;
    IXMLDOMNode oNodeSigValue = oNodeSig.selectSingleNode(".//*[local-name(.)='signatureValue']");
    // Get timestamp from a trusted timestamp service (fictitious).
    MyTrustedTimeStampService s = new MyTrustedTimeStampService();
    string strVerifiedTimeStamp = s.AddTimeStamp(oNodeSigValue.text);
    
    //Add the value returned from the timestamp service to the 
    //unsigned part of the signature block
    IXMLDOMNode oNodeObj = oNodeSig.selectSingleNode(".//*[local-name(.)='Object']");
    IXMLDOMNode oNode = oNodeObj.cloneNode(false);
    oNode.text = strVerifiedTimeStamp;
    oNodeObj.parentNode.appendChild(oNode);
    e.ReturnStatus = true;
}
```


