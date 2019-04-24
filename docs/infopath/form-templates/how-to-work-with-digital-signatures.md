---
title: Arbeiten mit digitalen Signaturen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- digitale Signaturen [InfoPath 2007], InfoPath 2007, digitale Signaturen
localization_priority: Normal
ms.assetid: fd13fb71-aecf-47bb-8a6b-db70bd90ceeb
description: Das Objektmodell des Microsoft. Office. InfoPath-Namespaces bietet Funktionen zum programmgesteuerten Arbeiten mit digitalen Signaturen.
ms.openlocfilehash: ea657f80f6e38a06a91e19c245eadc203c7c580c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303584"
---
# <a name="work-with-digital-signatures"></a>Arbeiten mit digitalen Signaturen

Das Objektmodell des [Microsoft. Office. InfoPath-](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) Namespaces bietet Funktionen zum programmgesteuerten Arbeiten mit digitalen Signaturen. 
  
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

Ein Ereignishandler für das [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) -Ereignis kann mit dem [SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) -Ereignisobjekt verwendet werden, das die folgenden Eigenschaften bereitstellt. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |Ruft die Datengruppe ab, die das [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) -Ereignis ausgelöst hat.  <br/> |
|[SignatureWizard](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |Ruft ab, ob das Dialogfeld **Digitale Signaturen** angezeigt werden soll, oder legt die Einstellung fest.  <br/> |
   
> [!NOTE]
> In dem verwalteten Codeobjektmodell von [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) , das im Lieferumfang von InfoPath 2003 enthalten ist, stellt das [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) -ereignisObjekt für das OnSign-Ereignis eine **XDocument** -Eigenschaft für den Zugriff auf die [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) ** XDocument** -Objekt des dem Ereignis zugeordneten Formulars. Dies ist bei Formularvorlagen, die mit InfoPath Forms Services oder InfoPath mithilfe des [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Objektmodells erstellt wurden, nicht erforderlich, da [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) auf die Objektmodellelemente der XmlForm-Klasse im Formularcode mithilfe des this-Objekts zugegriffen werden kann. ** **(C#) oder **Me** (Visual Basic)-Schlüsselwort. Um beispielsweise auf die [signierte](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse zuzugreifen, um zu bestimmen, ob ein Formular signiert ist, `this.Signed` können Sie entweder`Me.Signed.`
  
### <a name="collections-and-objects"></a>Auflistungen und Objekte

Das Objektmodell für digitale Signaturen stellt die folgenden Auflistungen bereit.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |Die Auflistung der [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) -Objekte in der Formularvorlage, die zur Entwurfszeit im InfoPath-Entwurfsmodus definiert sind.  <br/> Die [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) -Auflistung implementiert Eigenschaften, die für den Zugriff auf die einem Formular zugeordneten [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) -Objekte verwendet werden können. Auf [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) das einem Formular zugeordnete SignedDataBlockCollection-Objekt kann über die [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse zugegriffen werden.  <br/> |
|[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |Enthält eine Auflistung von [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) -Objekten für jedes [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) -Objekt im Formular.  <br/> Die [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) -Klasse implementiert Eigenschaften und eine Methode, die verwendet werden kann, um auf die zugeordneten [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) -Objekte eines Formulars zuzugreifen und eine Signatur zu erstellen. Auf [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) das SignatureCollection-Objekt, das einem [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) zugeordnet ist, kann mithilfe der [Signatures](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) -Eigenschaft zugegriffen werden.  <br/> Wenn Sie die [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) -Methode der [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) -Klasse verwenden, beachten Sie, dass die Signatur erst dann geschrieben wird, wenn die [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) -Methode für das [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) -Objekt aufgerufen wird. Diese Methoden können nur vom **Sign**-Ereignishandler einer vollständig vertrauenswürdigen Formularvorlage aus aufgerufen werden.  <br/> |
   
Das Objektmodell für digitale Signaturen stellt die folgenden Objekte bereit.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |Stellt eine signierbare Datengruppe in einem Formular dar. Das [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx)-Objekt stellt eine Reihe von Eigenschaften und eine Methode für die programmgesteuerte Interaktion mit einer signierbaren Datengruppe bereit.  <br/> |
|[Signatur](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |Stellt eine digitale Signatur dar, die einem Formular oder einer signierbaren Datengruppe in einem Formular hinzugefügt wurde. Das [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) -Objekt implementiert Eigenschaften, mit denen Informationen zur digitalen Signatur abgerufen werden können, sowie die [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) -Methode zum Schreiben des XML-Signatur Blocks und zum Berechnen des kryptografischen Hashwerts.  <br/> |
|[Certificate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |Stellt das digitale X.509-Zertifikat dar, das zum Erstellen der Signatur verwendet wurde.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Programmgesteuertes Arbeiten mit digitalen Signaturen

Das Objektmodell des [Microsoft. Office. InfoPath-](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) Namespaces stellt Elemente für die programmgesteuerte Interaktion mit digitalen Signaturen bereit. Insbesondere können voll vertrauenswürdige Formulare dem Signaturblock benutzerdefinierte Informationen hinzufügen, bevor ein Commit ausgeführt wird, entsprechend der folgenden Zeitachse: 
  
1. Der Benutzer wählt aus, dass einem Formular eine digitale Signatur hinzugefügt werden soll.
    
2. Das Dialogfeld **digitale Signaturen** wird angezeigt, der Benutzer klickt auf **Hinzufügen**und wählt dann die zu Signier Daten aus.
    
3. Das [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) -Ereignis für die vom [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) -Objekt dargestellten ausgewählten Daten wird ausgelöst, und die [Sign ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) -Methode des [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) -Objekts und die CreateSignature-Methode der [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) die Auflistung wird ausgeführt. 
    
4. Alle optionalen benutzerdefinierten Aktionen werden ausgeführt.
    
5. Die [Sign ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) -Methode des [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) -Objekts wird ausgeführt. 
    
6. Das Dialogfeld **Signieren** wird zum Eingeben eines Namens (oder Auswählen eines Signaturbildes), zum Auswählen eines Zertifikats für die Signierung und zum Eingeben von Kommentaren angezeigt. 
    
7. Wenn auf die Schaltfläche **Signieren** geklickt wird, wird die Signatur der Auflistung mit Signaturen für das Formular hinzugefügt, und die Nichtabstreitbarkeitsinformationen werden mit der Signatur aufgezeichnet und gespeichert (dies kann später angezeigt werden, indem im Dialogfeld **Digitale Signaturen** auf **Signiertes Formular anzeigen** und dann auf **Siehe die zusätzlichen gesammelten Signierungsinformationen** geklickt wird).
    
Im folgenden Beispiel wird die [Sign ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) -Methode aufgerufen, wenn der Benutzer die ausgewählten Daten signiert und die Signatur mit einem Timestamp-Wert gegenzeichnet, der von einem vertrauenswürdigen Zeitstempeldienst abgerufen wurde. 
  
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


