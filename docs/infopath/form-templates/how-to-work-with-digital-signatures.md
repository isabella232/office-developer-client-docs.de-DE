---
title: Arbeiten mit digitalen Signaturen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- digitale Signaturen [Infopath 2007] InfoPath 2007, digitale Signaturen
localization_priority: Normal
ms.assetid: fd13fb71-aecf-47bb-8a6b-db70bd90ceeb
description: Das Objektmodell des Microsoft.Office.InfoPath-Namespaces bietet Features für die Arbeit mit digitalen Signaturen programmgesteuert.
ms.openlocfilehash: 1277998edf4feb94da40d82372fd4d96fedf2d54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2018
ms.locfileid: "19790792"
---
# <a name="work-with-digital-signatures"></a>Arbeiten mit digitalen Signaturen

Das Objektmodell des [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespaces bietet Features für die Arbeit mit digitalen Signaturen programmgesteuert. 
  
## <a name="digital-signature-features"></a>Features für digitale Signaturen

Mithilfe der für digitale Signaturen von InfoPath bereitgestellten Features können Sie Folgendes ausführen:  
  
- Zulassen von Signaturen für das gesamte Formular oder für bestimmte Gruppen von Daten im Formular, die getrennt signiert werden können.
    
- Angeben bei jeder signierbaren Datengruppe, ob einzelne oder mehrere Signaturen zulässig sind und in welcher Beziehung diese zueinander stehen sollen. So können Sie beispielsweise angeben, ob es sich um parallele gemeinsame Signaturen handelt oder ob alle früheren Signaturen durch jede neue Signatur gegengezeichnet werden.
    
- Angeben einer Meldung, die angezeigt werden soll, wenn Benutzer das Formular signieren.
    
- Einfügen und Anzeigen einer Signatur im Dokument.  
    
- Überprüfbar Nichtabstreitbarkeit Informationen anzeigen, der jede Signatur, um eine höhere Sicherheit hinzugefügt wurde. Diese zusätzlichen Informationen, die eine Ansicht des Formulars enthält, wie es jeder signierenden Person vorgelegt wurde, ist Teil der Signatur und kann nicht entfernt werden, ohne dass die Signatur ungültig wird. Zu einem beliebigen Zeitpunkt können Sie diese Daten Denken Sie daran, indem Sie auf die Signatur im Formular, um das Dialogfeld **Digitale Signatur überprüfen** angezeigt werden soll. 
    
- Profitieren von einem umfangreicheren Objektmodell zum Arbeiten mit digitalen Signaturen. Fügen Sie dem Signaturblock in vollständig vertrauenswürdigen Formularen benutzerdefinierte Informationen zum Objektmodell für digitale Signaturen hinzu.  
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Übersicht über das Objektmodell für digitale Signaturen

### <a name="the-sign-event"></a>Sign-Ereignis

Das Objektmodell für digitale Signaturen stellt das folgende Ereignis bereit.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Anmelden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> |Tritt auf, nachdem eine Datengruppe zum Signieren ausgewählt wurde.  <br/> Mithilfe dieses Ereignisses können Sie die in der digitalen Signatur gespeicherten Daten bearbeiten. So können Sie beispielsweise Daten eines vertrauenswürdigen Zeitstempelservers oder eine serverseitige Gegensignatur der Transaktion hinzufügen. Sie können mit diesem Ereignis auch Signaturen blockieren, wenn der aktuelle Benutzer kein Mitglied einer bestimmten Gruppe ist.  <br/> |
   
### <a name="the-signeventargs-object"></a>SignEventArgs-Objekt

Ein Ereignishandler für das [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) -Ereignis kann mit [SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) -Event-Objekts verwendet werden, die die folgenden Eigenschaften bereitstellt. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[SignedDataBlock-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignedDataBlock.aspx) <br/> |Ruft die Datengruppe, die das [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) -Ereignis ausgelöst hat.  <br/> |
|[SignatureWizard](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.SignatureWizard.aspx) <br/> |Ruft ab oder legt fest, ob das Dialogfeld **Digitale Signaturen** angezeigt werden soll.  <br/> |
   
> [!NOTE]
> In der [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) Objektmodell für verwalteten Code, die mit InfoPath 2003 geliefert, bietet das [SignEvent](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.aspx) -Event-Objekt für das [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2.OnSign.aspx) -Ereignis eine **XDocument** -Eigenschaft für den Zugriff auf die ** XDocument** -Objekt des Formulars mit dem Ereignis verknüpft ist. Dies ist nicht mit Formularvorlagen mit InfoPath Forms Services oder InfoPath mithilfe des [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Objektmodells, da die Elemente des Objektmodells der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse zugegriffen werden können, im Formularcode die **mit diesem erstellten erforderlich **(C#) oder das Schlüsselwort **Me** (Visual Basic). Beispielsweise Zugriff auf die [Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse, um festzustellen, ob ein Formular signiert ist, geben Sie entweder `this.Signed` oder`Me.Signed.`
  
### <a name="collections-and-objects"></a>Auflistungen und Objekte

Das Objektmodell für digitale Signaturen stellt die folgenden Auflistungen bereit.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) <br/> |Die Auflistung der [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) -Objekte in der Formularvorlage gemäß zur Entwurfszeit im InfoPath-Entwurfsmodus definiert.  <br/> Die [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) -Auflistung implementiert Eigenschaften, die auf einem Formular zugeordneten [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) -Objekte verwendet werden können. Das [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) -Objekt, das einem Formular zugeordnet ist, kann über die [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse zugegriffen werden.  <br/> |
|[SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) <br/> |Enthält eine Auflistung von [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) -Objekten für jedes [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) -Objekt im Formular.  <br/> Die [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) -Klasse implementiert Eigenschaften und eine Methode, die auf einem Formular zugeordneten [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) -Objekte zuzugreifen und zum Erstellen einer Signatur verwendet werden kann. Das einem [SignedDataBlock-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) zugeordnete [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) -Objekt erfolgt mithilfe der [Signatures](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Signatures.aspx) -Eigenschaft.  <br/> Beachten Sie bei der Sie die [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) -Methode der [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) -Klasse verwenden, denken Sie daran, die die Signatur bis das [Zeichen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) nicht geschrieben werden-Methode auf das [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) -Objekt aufgerufen wird. Diese Methoden können nur aus der Ereignishandler **Signieren** einer voll vertrauenswürdigen Formularvorlage aufgerufen werden.  <br/> |
   
Das Objektmodell für digitale Signaturen stellt die folgenden Objekte bereit.
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[SignedDataBlock-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |Stellt einen Satz signierbarer Daten in einem Formular dar. Das [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) -Objekt bietet eine Reihe von Eigenschaften und eine Methode, die für die programmgesteuerte Interaktion mit einem Satz signierbarer Daten verwendet werden können.  <br/> |
|[Signatur](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |Stellt eine digitale Signatur, die an ein Formular oder eine signierbare Datengruppe in einem Formular hinzugefügt wurde. Das [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) -Objekt implementiert Eigenschaften, die zum Abrufen von Informationen über die digitale Signatur und die [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) -Methode zum Schreiben des XML-Blocks mit digitalen Signaturen und dessen Wert kryptografischen Hash computing verwendet werden können.  <br/> |
|[Zertifikat](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Certificate.aspx) <br/> |Stellt das digitale X.509-Zertifikat dar, das zum Erstellen der Signatur verwendet wurde.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Programmgesteuertes Arbeiten mit digitalen Signaturen

Das Objektmodell des [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace stellt Member für die programmgesteuerte Interaktion mit digitalen Signaturen bereit. Insbesondere können voll vertrauenswürdige Formulare hinzufügen benutzerdefinierten Informationen dem Signaturblock bevor es gespeichert wird gemäß der folgenden Zeitplan: 
  
1. Der Benutzer wählt aus, dass einem Formular eine digitale Signatur hinzugefügt werden soll.
    
2. Das Dialogfeld **Digitale Signaturen** wird angezeigt, die der Benutzer klickt auf **Hinzufügen**und wählt dann die zu signierenden Daten.
    
3. Das für die ausgewählten Daten, die durch das [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) -Objekt dargestellten [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) -Ereignis wird ausgelöst, und die [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) -Methode des [SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) -Objekt und die [CreateSignature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.CreateSignature.aspx) -Methode, der die [SignatureCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignatureCollection.aspx) Auflistung ausgeführt werden. 
    
4. Alle optionalen benutzerdefinierten Aktionen werden ausgeführt.
    
5. Die [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.Sign.aspx) -Methode des [Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) -Objekts wird ausgeführt. 
    
6. Das Dialogfeld **Signieren** wird angezeigt, für die Eingabe eines Namens (oder Auswählen eines signaturbildes), Auswählen eines Zertifikats für die Signierung und zum Eingeben von Kommentaren. 
    
7. Wenn die Schaltfläche **Signieren** geklickt wird, wird die Signatur der Auflistung von Signaturen für das Formular hinzugefügt und die Nichtabstreitbarkeit Informationen erfasst und gespeichert, die mit der Signatur (die weiter unten angezeigt werden kann, indem Sie **Signiertes Formular anzeigen** auf die ** Digitale Signaturen** im Dialogfeld klicken und dann auf **finden Sie unter der zusätzliche Signaturinformationen, die gesammelt wurden**).
    
Im folgenden Beispiel wird die [Sign()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.Sign.aspx) -Methode auf, wenn der Benutzer die ausgewählten Daten signiert und die Signatur mit einem Zeitstempelwert, der von einem vertrauenswürdigen Zeitstempeldienst abgerufen versieht. 
  
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


