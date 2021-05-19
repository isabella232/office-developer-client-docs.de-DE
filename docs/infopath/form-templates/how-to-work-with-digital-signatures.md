---
title: Arbeiten mit digitalen Signaturen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- digitale Signaturen [infopath 2007],InfoPath 2007, digitale Signaturen
localization_priority: Normal
ms.assetid: fd13fb71-aecf-47bb-8a6b-db70bd90ceeb
description: Das Objektmodell von Microsoft. Office. Der InfoPath-Namespace bietet Features zum programmgesteuerten Arbeiten mit digitalen Signaturen.
ms.openlocfilehash: ea657f80f6e38a06a91e19c245eadc203c7c580c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425575"
---
# <a name="work-with-digital-signatures"></a>Arbeiten mit digitalen Signaturen

Das Objektmodell der [Microsoft.Office. Der InfoPath-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) bietet Features zum programmgesteuerten Arbeiten mit digitalen Signaturen. 
  
## <a name="digital-signature-features"></a>Features für digitale Signaturen

Mithilfe der für digitale Signaturen von InfoPath bereitgestellten Features können Sie Folgendes ausführen: 
  
- Zulassen von Signaturen für das gesamte Formular oder für bestimmte Gruppen von Daten im Formular, die getrennt signiert werden können.
    
- Angeben bei jeder signierbaren Datengruppe, ob einzelne oder mehrere Signaturen zulässig sind und in welcher Beziehung diese zueinander stehen sollen. So können Sie beispielsweise angeben, ob es sich um parallele gemeinsame Signaturen handelt oder ob alle früheren Signaturen durch jede neue Signatur gegengezeichnet werden.
    
- Angeben einer Meldung, die angezeigt werden soll, wenn Benutzer das Formular signieren.
    
- Einfügen und Anzeigen einer Signatur im Dokument. 
    
- Anzeigen überprüfbarer Nichtabstreitbarkeitsinformationen, die jeder Signatur zur Steigerung der Sicherheit hinzugefügt wurden. Diese zusätzlichen Informationen, die eine Ansicht des Formulars einschließen, wie es jeder signierenden Person vorgelegt wurde, sind ein Bestandteil der Signatur und können nicht entfernt werden, ohne die Signatur ungültig zu machen. Sie können diese Daten jederzeit erneut aufrufen, indem Sie auf die Signatur im Formular klicken, um das Dialogfeld **Digitale Signatur überprüfen** anzuzeigen. 
    
- Profitieren von einem umfangreicheren Objektmodell zum Arbeiten mit digitalen Signaturen. Fügen Sie dem Signaturblock in vollständig vertrauenswürdigen Formularen benutzerdefinierte Informationen zum Objektmodell für digitale Signaturen hinzu.  
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Übersicht über das Objektmodell für digitale Signaturen

### <a name="the-sign-event"></a>Sign-Ereignis

Das Objektmodell für digitale Signaturen stellt das folgende Ereignis bereit.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |Tritt auf, nachdem eine Datengruppe zum Signieren ausgewählt wurde.  <br/> Mithilfe dieses Ereignisses können Sie die in der digitalen Signatur gespeicherten Daten bearbeiten. So können Sie beispielsweise Daten eines vertrauenswürdigen Zeitstempelservers oder eine serverseitige Gegensignatur der Transaktion hinzufügen. Sie können mit diesem Ereignis auch Signaturen blockieren, wenn der aktuelle Benutzer kein Mitglied einer bestimmten Gruppe ist.  <br/> |
   
### <a name="the-signeventargs-object"></a>SignEventArgs-Objekt

Ein Ereignishandler für das [Sign-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) kann mit dem [SignEventArgs-Ereignisobjekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) verwendet werden, das die folgenden Eigenschaften bietet. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |Ruft den Satz von Daten ab, der das [Sign-Ereignis ausgelöst](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) hat.  <br/> |
|[SignatureWizard](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |Ruft ab, ob das Dialogfeld **Digitale Signaturen** angezeigt werden soll, oder legt die Einstellung fest.  <br/> |
   
> [!NOTE]
> Im [Microsoft.Office.Interop.InfoPath.SemiTrust-Objektmodell](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) mit verwalteten Code, das mit InfoPath 2003 ausgeliefert wurde, stellt das [SignEvent-Ereignisobjekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) für das [OnSign-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) eine **XDocument-Eigenschaft** für den Zugriff auf das **XDocument-Objekt** des Formulars zur Verfügung, das dem Ereignis zugeordnet ist. Dies ist bei Formularvorlagen, die mit InfoPath Forms Services oder InfoPath mithilfe von [Microsoft.Office. InfoPath-Objektmodell,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) da auf die Objektmodellmmitglieder der [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) im Formularcode mithilfe des Schlüsselworts this **(C#)** oder **Me** (Visual Basic) zugegriffen werden kann. Wenn Sie beispielsweise auf die [Signed-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) der [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) zugreifen möchten, um zu ermitteln, ob ein Formular signiert ist, können Sie entweder oder `this.Signed``Me.Signed.`
  
### <a name="collections-and-objects"></a>Auflistungen und Objekte

Das Objektmodell für digitale Signaturen stellt die folgenden Auflistungen bereit.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |Die Auflistung der [SignedDataBlock-Objekte](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) in der Formularvorlage, wie zur Entwurfszeit im InfoPath-Entwurfsmodus definiert.  <br/> Die [SignedDataBlockCollection-Auflistung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) implementiert Eigenschaften, die für den Zugriff auf [die signedDataBlock-Objekte verwendet](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) werden können, die einem Formular zugeordnet sind. Auf das einem Formular zugeordnete [SignedDataBlockCollection-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) kann über die [SignedDataBlocks-Eigenschaft der](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) [XmlForm-Klasse zugegriffen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) werden.  <br/> |
|[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |Enthält eine Auflistung von [Signature-Objekten](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) für jedes [SignedDataBlock-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) im Formular.  <br/> Die [SignatureCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) implementiert Eigenschaften und eine Methode, mit der auf die zugeordneten [Signature-Objekte](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) eines Formulars zugegriffen und eine Signatur erstellt werden kann. Auf [das SignatureCollection-Objekt,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) das einem [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) zugeordnet ist, kann mithilfe der [Signatures-Eigenschaft zugegriffen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) werden.  <br/> Wenn Sie die [CreateSignature-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) der [SignatureCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) verwenden, beachten Sie, dass die Signatur erst geschrieben wird, wenn die [Sign-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) für das [Signature-Objekt aufgerufen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) wird. Diese Methoden können nur vom **Sign**-Ereignishandler einer vollständig vertrauenswürdigen Formularvorlage aus aufgerufen werden.  <br/> |
   
Das Objektmodell für digitale Signaturen stellt die folgenden Objekte bereit.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |Stellt eine signierbare Datengruppe in einem Formular dar. Das [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx)-Objekt stellt eine Reihe von Eigenschaften und eine Methode für die programmgesteuerte Interaktion mit einer signierbaren Datengruppe bereit.<br/> |
|[Signatur](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |Stellt eine digitale Signatur dar, die einem Formular oder einer signierbaren Datengruppe in einem Formular hinzugefügt wurde. Das [Signature-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) implementiert Eigenschaften, die verwendet werden können, um Informationen zur digitalen Signatur abzurufen, und die [Sign-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) zum Schreiben des digitalen #A0 und zum Berechnen des kryptografischen Hashwerts.  <br/> |
|[Zertifikat](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |Stellt das digitale X.509-Zertifikat dar, das zum Erstellen der Signatur verwendet wurde.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Programmgesteuertes Arbeiten mit digitalen Signaturen

Das Objektmodell der [Microsoft.Office. Der InfoPath-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) bietet Mitgliedern die programmgesteuerte Interaktion mit digitalen Signaturen. Insbesondere voll vertrauenswürdige Formulare können dem Signaturblock benutzerdefinierte Informationen hinzufügen, bevor er gemäß der folgenden Zeitachse gebunden wird: 
  
1. Der Benutzer wählt aus, dass einem Formular eine digitale Signatur hinzugefügt werden soll.
    
2. Das **Dialogfeld Digitale Signaturen** wird angezeigt, der Benutzer klickt auf **Hinzufügen** und wählt dann die zu signierenden Daten aus.
    
3. Das [Sign-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) für die ausgewählten Daten, die durch das [SignedDataBlock-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) dargestellt werden, wird ausgelöst, und die [Sign()-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) des [SignedDataBlock-Objekts](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) und die [CreateSignature-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) der [SignatureCollection-Auflistung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) werden ausgeführt. 
    
4. Alle optionalen benutzerdefinierten Aktionen werden ausgeführt.
    
5. Die [Sign()-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) des [Signature-Objekts](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) wird ausgeführt. 
    
6. Das Dialogfeld **Signieren** wird zum Eingeben eines Namens (oder Auswählen eines Signaturbildes), zum Auswählen eines Zertifikats für die Signierung und zum Eingeben von Kommentaren angezeigt. 
    
7. Wenn auf die Schaltfläche **Signieren** geklickt wird, wird die Signatur der Auflistung mit Signaturen für das Formular hinzugefügt, und die Nichtabstreitbarkeitsinformationen werden mit der Signatur aufgezeichnet und gespeichert (dies kann später angezeigt werden, indem im Dialogfeld **Digitale Signaturen** auf **Signiertes Formular anzeigen** und dann auf **Siehe die zusätzlichen gesammelten Signierungsinformationen** geklickt wird).
    
Im folgenden Beispiel wird die [Sign()-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) aufgerufen, wenn der Benutzer die ausgewählten Daten signiert und die Signatur mit einem Zeitstempelwert gegensigniert, der von einem vertrauenswürdigen Zeitstempeldienst abgerufen wurde. 
  
```cs
public void FormEvents_Sign(object sender, SignEventArgs e)
{
   // Add a new Signature object to the SignedDataBlockCollection.
   Signature thisSignature = 
      e.SignedDataBlock.Signatures.CreateSignature();
   // Write the XML digital signature block and compute hash
   // for signed data.
   thisSignature.Sign();
   // Countersign the signature with a trusted timestamp.
   // Get the XML node storing the signature block.
   XPathNavigator oNodeSig = thisSignature.SignatureBlockXmlNode;
   XPathNavigator oNodeSigValue = 
      oNodeSig.SelectSingleNode(
      ".//*[local-name(.)='signatureValue']");
   // Get timestamp from a trusted timestamp service (fictitious).
   MyTrustedTimeStampService s = new MyTrustedTimeStampService();
   string strVerifiedTimeStamp = s.AddTimeStamp(oNodeSigValue.Value);
   // Add the value returned from the timestamp service to the 
   // unsigned part of the signature block.
   XPathNavigator oNodeObj = 
      oNodeSig.SelectSingleNode(".//*[local-name(.)='Object']");
   XPathNavigator oNode = oNodeObj.Clone();
   oNode.SetValue(strVerifiedTimeStamp);
   oNodeObj.MoveToParent();
   oNodeObj.AppendChild(oNode);
   e.SignatureWizard = false;
}
```

```vb
Public Sub FormEvents_Sign(ByVal sender As Object, _
   ByVal e As SignEventArgs)
   ' Add a new Signature object to the SignedDataBlockCollection.
   Dim thisSignature As Signature = 
      e.SignedDataBlock.Signatures.CreateSignature
   ' Write the XML digital signature block and compute hash
   ' for signed data.
   thisSignature.Sign()
   ' Countersign the signature with a trusted timestamp.
   ' Get the XML node storing the signature block
   Dim oNodeSig As XPathNavigator  = _
      thisSignature.SignatureBlockXmlNode
   Dim oNodeSigValue As XPathNavigator  = _
      oNodeSig.SelectSingleNode(_
      ".//*[local-name(.)='signatureValue']")
   ' Get timestamp from a trusted timestamp service (fictitious).
   Dim s As MyTrustedTimeStampService = New MyTrustedTimeStampService()
   Dim strVerifiedTimeStamp As String  = _
      s.AddTimeStamp(oNodeSigValue.Value)
   ' Add the value returned from the timestamp service to the 
   ' unsigned part of the signature block.
   Dim oNodeObj As XPathNavigator  = 
      oNodeSig.SelectSingleNode(".//*[local-name(.)='Object']")
   Dim oNode As XPathNavigator  = oNodeObj.Clone()
   oNode.SetValue(strVerifiedTimeStamp)
   oNodeObj.MoveToParent()
   oNodeObj.AppendChild(oNode)
   e.SignatureWizard = False
```


