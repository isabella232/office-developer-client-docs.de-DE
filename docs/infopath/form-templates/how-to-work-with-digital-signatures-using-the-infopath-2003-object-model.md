---
title: Arbeiten mit digitalen Signaturen mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Digitale Signaturen [infopath 2007], infopath 2003-kompatible Formularvorlagen,InfoPath 2003-kompatible Formularvorlagen, digitale Signaturen
localization_priority: Normal
ms.assetid: d6318238-fd45-4854-a3c9-c27c5685bd6b
description: Das InfoPath 2003-kompatible Objektmodell bietet Features zum programmgesteuerten Verwenden von digitalen Signaturen.
ms.openlocfilehash: 86e2c85c7515c896612df09b6186462480ceff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433444"
---
# <a name="work-with-digital-signatures-using-the-infopath-2003-object-model"></a>Arbeiten mit digitalen Signaturen mithilfe des InfoPath 2003-Objektmodells

Das InfoPath 2003-kompatible Objektmodell bietet Features zum programmgesteuerten Verwenden von digitalen Signaturen.
  
## <a name="digital-signature-features"></a>Features für digitale Signaturen

Mithilfe der Features für digitale Signaturen in InfoPath können Sie Folgendes ausführen: 
  
- Ermöglichen von Signaturen für das gesamte Formular oder für bestimmte Gruppen von Daten im Formular, die getrennt signiert werden können.
    
- Angeben bei jeder signierbaren Datengruppe, ob einzelne oder mehrere Signaturen zulässig sind und in welcher Beziehung diese zueinander stehen sollen. So können Sie beispielsweise angeben, ob es sich um parallele gemeinsame Signaturen handelt oder ob alle früheren Signaturen durch jede neue Signatur gegengezeichnet werden.
    
- Angeben einer Meldung, die angezeigt werden soll, wenn Benutzer das Formular signieren.
    
- Einfügen und Anzeigen einer Signatur im Dokument. 
    
- Anzeigen überprüfbarer Nichtabstreitbarkeitsinformationen, die jeder Signatur zur Steigerung der Sicherheit hinzugefügt wurden. Diese zusätzlichen Informationen, die eine Ansicht des Formulars einschließen, wie es jeder signierenden Person vorgelegt wurde, sind ein Bestandteil der Signatur und können nicht entfernt werden, ohne die Signatur ungültig zu machen. Sie können diese Daten jederzeit erneut aufrufen, indem Sie auf die Signatur im Formular klicken, um das Dialogfeld **Digitale Signatur überprüfen** anzuzeigen. 
    
- Profitieren von einem umfangreicheren Objektmodell zum Arbeiten mit digitalen Signaturen. Fügen Sie dem Signaturblock in vollständig vertrauenswürdigen Formularen benutzerdefinierte Informationen zum Objektmodell für digitale Signaturen hinzu.  
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Übersicht über das Objektmodell für digitale Signaturen

### <a name="events"></a>Ereignisse

Das Objektmodell für digitale Signaturen stellt das folgende Ereignis bereit.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |Tritt ein, nachdem eine signierbare Datengruppe zum Signieren ausgewählt wurde.  <br/> Mithilfe dieses Ereignisses können Sie die in der digitalen Signatur gespeicherten Daten bearbeiten. So können Sie beispielsweise Daten eines vertrauenswürdigen Zeitstempelservers oder eine serverseitige Gegensignatur der Transaktion hinzufügen. Sie können mit diesem Ereignis auch Signaturen blockieren, wenn der aktuelle Benutzer kein Mitglied einer bestimmten Gruppe ist.  <br/> |
   
Das **OnSign-Ereignis** gibt einen Verweis auf das [SignEventObject-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) zurück, das die folgenden Eigenschaften bietet. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.ReturnStatus.aspx) <br/> |Ruft einen Wert vom Typ **Boolean** ab, der den Rückgabestatus des **OnSign**-Ereignisses angibt, oder legt diesen Wert fest.  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.SignedDataBlock.aspx) <br/> |Ruft den signierten Datenblock ab, durch den das **OnSign**-Ereignis ausgelöst wurde.  <br/> |
|[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.XDocument.aspx) <br/> |Ruft einen Verweis auf das **XDocument**-Objekt ab, das dem **OnSign**-Ereignis zugeordnet ist.  <br/> |
   
### <a name="collections-and-objects"></a>Auflistungen und Objekte

Das Objektmodell für digitale Signaturen stellt die folgenden Auflistungen bereit.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[SignedDataBlocksCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlocksCollection.aspx) <br/> |Die Auflistung der [SignedDataBlockObject-Objekte](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) in der Formularvorlage, wie in der Formulardefinitionsdatei (XSF) definiert.  <br/> Die **SignedDataBlocksCollection**-Auflistung implementiert Eigenschaften, die den Zugriff auf die einem Formular zugeordneten **SignedDataBlockObjects**-Objekte ermöglichen. Auf **die SignedDataBlocks-Auflistung** kann über die [SignedDataBlocks-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) des [XDocument-Objekts zugegriffen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) werden.  <br/> |
|[SignaturesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignaturesCollection.aspx) <br/> |Enthält eine Auflistung von [SignatureObject-Objekten](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) für jedes **SignedDataBlockObject-Objekt** im Formular.  <br/> Die **SignaturesCollection**-Auflistung implementiert Eigenschaften und eine Methode, um auf die zugeordneten **SignatureObject**-Objekte eines Formulars zuzugreifen und eine Signatur zu erstellen. Der Zugriff darauf ist über das **SignedDataBlockObject**-Objekt möglich. <br/> Wenn Sie die [Create-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) der **SignaturesCollection-Auflistung** verwenden, beachten Sie, dass die Signatur erst geschrieben wird, wenn die [Sign-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) für das **SignatureObject-Objekt aufgerufen** wird. Diese Methoden können nur vom **OnSign**-Ereignishandler einer vollständig vertrauenswürdigen Formularvorlage aus aufgerufen werden.  <br/> |
   
Das Objektmodell für digitale Signaturen stellt die folgenden Objekte bereit.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) <br/> |Stellt eine signierbare Datengruppe in einem Formular dar. Das **SignedDataBlock**-Objekt stellt eine Reihe von Eigenschaften und eine Methode für die programmgesteuerte Interaktion mit einer signierbaren Datengruppe bereit.<br/> |
|[SignatureObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) <br/> |Stellt eine digitale Signatur dar, die einem Formular oder einer signierbaren Datengruppe in einem Formular hinzugefügt wurde. Die **SignatureObject-Auflistung** implementiert Eigenschaften, die verwendet werden können, um Informationen zur digitalen Signatur abzurufen, und die [Sign-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) zum Schreiben des digitalen #A0 und zum Berechnen des kryptografischen Hashwerts.  <br/> |
|[CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) <br/> |Stellt das digitale X.509-Zertifikat dar, das zum Erstellen der Signatur verwendet wurde.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Programmgesteuertes Arbeiten mit digitalen Signaturen

Das InfoPath 2003-kompatible Objektmodell stellt Member für die programmgesteuerte Interaktion mit digitalen Signaturen bereit. So können insbesondere in vollständig vertrauenswürdigen Formularen benutzerdefinierte Informationen dem Signaturblock hinzugefügt werden, bevor ein Commit für ihn ausgeführt wird. Dies geschieht entsprechend dem folgenden Zeitplan:
  
1. Der Benutzer entscheidet, dass einem Formular eine digitale Signatur hinzugefügt werden soll.
    
2. Das erste Fenster desAssistenten für digitale Signaturen wird angezeigt. 
    
3. Das **OnSign**-Ereignis für die ausgewählten Daten, die durch das **SignedDataBlockObject**-Objekt dargestellt werden, wird ausgelöst. Die **Sign**-Methode des **SignedDataBlockObject**-Objekts und die **Create**-Methode der **SignaturesCollection**-Auflistung werden ausgeführt. 
    
4. Alle optionalen benutzerdefinierten Aktionen werden ausgeführt.
    
5. Die **Sign**-Methode des **SignatureObject**-Objekts wird ausgeführt. 
    
6. Das zweite und dritte Fenster des Assistenten werden angezeigt, in denen ein Zertifikat zum Signieren ausgewählt und Kommentare eingegeben werden können.
    
7. Die Nichtabstreitbarkeitsinformationen werden angezeigt (und können später im Dialogfeld **Digitale Signatur überprüfen** angezeigt werden). 
    
8. Beim Klicken auf die Schaltfläche **Signieren** wird die Signatur der Auflistung von Signaturen für das Formular hinzugefügt. 
    
Im folgenden Beispiel wird das Dialogfeld **Signieren** aufgerufen und verwendet, um eine Signatur mit einem Zeitstempelwert gegenzuzeichnen, der von einem vertrauenswürdigen Zeitstempeldienst abgerufen wurde. 
  
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


