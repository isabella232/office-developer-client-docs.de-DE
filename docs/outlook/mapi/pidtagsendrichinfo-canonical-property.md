---
title: PidTagSendRichInfo (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSendRichInfo
api_type:
- COM
ms.assetid: e85fc766-197a-484f-b600-68cd28a052a2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 11d6b8cc633707512d8f4cb7447076f88dd0f74e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599438"
---
# <a name="pidtagsendrichinfo-canonical-property"></a>PidTagSendRichInfo (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn der Empfänger alle Nachrichteninhalte empfangen kann, einschließlich RTF-Objekte (Rich Text Format) und OLE-Objekte (Object Linking and Embedding). 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SEND_RICH_INFO  <br/> |
|Kennung:  <br/> |0x3A40  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Es wird empfohlen, dass Verteilerlisten- und Messagingbenutzerobjekte diese Eigenschaft verfügbar machen. 
  
Diese Eigenschaft gibt an, ob der Absender den Empfänger als MAPI-aktiviert betrachtet. 
  
Wenn diese Eigenschaft auf TRUE festgelegt ist, können Transport und Gateway den vollständigen Inhalt der Nachricht übertragen, einschließlich RTF- und OLE-Objekten. Transport provider and gateway should use Transport Neutral Encapsulation Format (TNEF) to encapsulate any properties that are not native to all the messaging systems involved. 
  
Wenn diese Eigenschaft auf FALSE festgelegt ist, können der Transportanbieter und das Gateway Nachrichteninhalte verwerfen, die ihre systemeigenen Clients nicht verwenden können. Wenn die Clients beispielsweise RTF nicht unterstützen, kann der Transportanbieter nur Nur-Text senden. 
  
Wenn diese Eigenschaft nicht festgelegt ist, wird das Standardverhalten durch die Implementierung des Transportanbieters, des Nachrichtenübertragungs-Agents (Message Transfer Agent, MTA) oder des Gateways bestimmt. Adressbuchanbieter müssen diese Eigenschaft nicht unterstützen. Beispielsweise kann ein eng gekoppelter Adressbuch- und Transportanbieter TNEF senden, aber niemals RTF verwenden. 
  
Der Client sollte nicht davon ausgehen, dass der Transportanbieter und das Gateway TNEF auf eigene Initiative verwenden. Einige Transportanbieter und Gateways, die TNEF unterstützen, übertragen sie ohne Berücksichtigung des Werts dieser Eigenschaft, andere weisen jedoch das Erstellen oder Senden von TNEF zurück, wenn sie nicht auf TRUE festgelegt ist. 
  
> [!NOTE]
> Die Einstellung dieser Eigenschaft und die auf ihrem Wert basierenden Entscheidungen erfolgen auf Empfängerbasis. 
  
MapI legt den Wert standardmäßig auf TRUE fest. Ein Client, der [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) aufruft, oder ein Anbieter, der [IMAPISupport::CreateOneOff aufruft,](imapisupport-createoneoff.md) kann das **MAPI_SEND_NO_RICH_INFO** Bit im  _ulFlags-Parameter_ festlegen, wodurch die MAPI diese Eigenschaft auf FALSE festlegt. Von der Benutzeroberfläche erstellte Einmalige verwenden den in der Erstellungsvorlage angegebenen Wert. 
  
Bei Aufrufen der [IAddrBook::ResolveName-Methode,](iaddrbook-resolvename.md) wenn der Name nicht aufgelöst werden kann, aber als Internetadresse (SMTP) interpretiert werden kann, wird diese Eigenschaft auf FALSE festgelegt. Damit der Anzeigename als Internetadresse angegeben werden kann, muss der Anzeigename des nicht aufgelösten Eintrags im Format X@Y sein. Z, z. B. "pete@pinecone.com". 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> von Internetstandard-E-Mail-Konventionen zu Nachrichtenobjekten.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[PidTagAttachDataObject (kanonische Eigenschaft)](pidtagattachdataobject-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

