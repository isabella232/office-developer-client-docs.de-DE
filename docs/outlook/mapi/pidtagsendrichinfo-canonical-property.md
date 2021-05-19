---
title: PidTagSendRichInfo (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendRichInfo
api_type:
- COM
ms.assetid: e85fc766-197a-484f-b600-68cd28a052a2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a7ad27d757d4ed6df58c597bf17d9e5412f83457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342518"
---
# <a name="pidtagsendrichinfo-canonical-property"></a>PidTagSendRichInfo (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn der Empfänger alle Nachrichteninhalte empfangen kann, einschließlich Rich Text Format (RTF) und Object Linking and Embedding (OLE)-Objekte. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SEND_RICH_INFO  <br/> |
|Kennung:  <br/> |0x3A40  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>Hinweise

Es wird empfohlen, dass Verteilerlisten- und Messagingbenutzerobjekte diese Eigenschaft verfügbar machen. 
  
Diese Eigenschaft gibt an, ob der Absender den Empfänger als MAPI-aktiviert betrachtet. 
  
Wenn diese Eigenschaft auf TRUE festgelegt ist, können der Transport und das Gateway den vollständigen Inhalt der Nachricht übertragen, einschließlich RTF- und OLE-Objekten. Der Transportanbieter und das Gateway sollten das TNEF (Transport Neutral Encapsulation Format) verwenden, um alle Eigenschaften zu kapseln, die nicht für alle beteiligten Messagingsysteme systemeigene Sind. 
  
Wenn diese Eigenschaft auf FALSE festgelegt ist, können der Transportanbieter und das Gateway Nachrichteninhalte verwerfen, die von ihren systemeigenen Clients nicht verwendet werden können. Wenn die Clients z. B. RTF nicht unterstützen, kann der Transportanbieter nur Nur-Text senden. 
  
Wenn diese Eigenschaft nicht festgelegt ist, wird das Standardverhalten durch die Implementierung des Transportanbieters, des Nachrichtenübertragungs-Agents (Message Transfer Agent, MTA) oder des Gateways bestimmt. Adressbuchanbieter müssen diese Eigenschaft nicht unterstützen. Beispielsweise können ein eng gekoppelte Adressbuch- und Transportanbieter TNEF senden, aber rtF nie verwenden. 
  
Der Client sollte nicht davon ausgehen, dass der Transportanbieter und das Gateway TNEF von sich aus verwenden. Einige Transportanbieter und Gateways, die TNEF unterstützen, übertragen sie ohne Rücksicht auf den Wert dieser Eigenschaft, andere ablehnen jedoch, TNEF zu erstellen oder zu senden, wenn sie nicht auf TRUE festgelegt ist. 
  
> [!NOTE]
> Die Einstellung dieser Eigenschaft und die Entscheidungen basierend auf ihrem Wert erfolgen pro Empfänger. 
  
Standardmäßig legt MAPI den Wert auf TRUE fest. Ein Client, der [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) aufruft, oder ein Anbieter, der [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) aufruft, kann das **MAPI_SEND_NO_RICH_INFO-Bit** im  _ulFlags-Parameter_ festlegen, wodurch MAPI diese Eigenschaft auf FALSE festlegen kann. Von der Benutzeroberfläche erstellte Einmalvorlagen verwenden den in der Erstellungsvorlage angegebenen Wert. 
  
Bei Aufrufen der [IAddrBook::ResolveName-Methode,](iaddrbook-resolvename.md) wenn der Name nicht aufgelöst werden kann, aber als Internetadresse (SMTP) interpretiert werden kann, wird diese Eigenschaft auf FALSE festgelegt. Um als Internetadresse ausgelegt zu werden, muss der Anzeigename des nicht aufgelösten Eintrags im Format X@Y. Z, z. B. "pete@pinecone.com". 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> von Internetstandard-E-Mail-Konventionen zu Nachrichtenobjekten.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagAttachDataObject (kanonische Eigenschaft)](pidtagattachdataobject-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

