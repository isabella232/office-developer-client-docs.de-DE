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
ms.openlocfilehash: a1db4ba7a70695b17631ca13f1728043be8164bd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575966"
---
# <a name="pidtagsendrichinfo-canonical-property"></a>PidTagSendRichInfo (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn der Empfänger alle Nachrichteninhalt, einschließlich Rich Text Format (RTF) und Objekten Object Linking and Embedding (OLE) empfangen kann. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SEND_RICH_INFO  <br/> |
|Kennung:  <br/> |0x3A40  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Es wird empfohlen, dass diese Eigenschaft Verteilerliste und messaging User-Objekte verfügbar machen. 
  
Diese Eigenschaft gibt an, ob der Absender den Empfänger zu MAPI-fähigen betrachtet. 
  
Wenn diese Eigenschaft auf TRUE festgelegt ist, können die Transport- und Gateway des gesamten Inhalts der Nachricht, einschließlich RTF und OLE-Objekte übertragen. Der Adressbuchhierarchie und Gateway sollte Transport Neutral Encapsulation Format (TNEF) verwenden, um alle Eigenschaften kapseln, die nicht für alle der Messagingsysteme beteiligten systemeigene sind. 
  
Wenn diese Eigenschaft auf FALSE festgelegt ist, können der Adressbuchhierarchie und Gateway Nachrichteninhalt verwerfen, die systemeigene-Clients verwendet werden können. Beispielsweise kann die Clients RTF nicht unterstützen, der Adressbuchhierarchie nur-Text senden. 
  
Wenn diese Eigenschaft nicht festgelegt ist, wird durch die Implementierung der Adressbuchhierarchie, Message Transfer Agent (MTA) oder Gateway Standardverhalten bestimmt. Von adressbuchanbietern implementierte sind zur Unterstützung von dieser Eigenschaft nicht erforderlich. Beispielsweise können ein eng gekoppelten Adresse Adressbuch und Transport Anbieter senden TNEF jedoch nie RTF-Format verwenden. 
  
Der Client sollte nicht der Adressbuchhierarchie voraussetzen und Gateway TNEF auf eigene Initiative verwenden. Einige Transportanbieter und Gateways, die Unterstützung von TNEF ohne Berücksichtigung des Werts dieser Eigenschaft übertragen, aber andere ablehnen, zu erstellen oder TNEF senden, wenn sie nicht auf TRUE festgelegt ist. 
  
> [!NOTE]
> Die Einstellung dieser Eigenschaft und die Entscheidungen basierend auf seinen Wert sind für einzelne pro Empfänger. 
  
Der Wert von MAPI wird standardmäßig auf "true" festgelegt. Ein Aufruf von [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) oder einen Anbieter Aufrufen [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) Client kann das **MAPI_SEND_NO_RICH_INFO** Bit im Parameter _UlFlags_ festgelegt, MAPI, um diese Eigenschaft auf FALSE festgelegt. Von der Benutzeroberfläche erstellt Fly verwenden Sie den Wert durch die Vorlage erstellen angegeben. 
  
Wenn der Name kann nicht aufgelöst werden, aber als eine IP-Adresse (SMTP) interpretiert werden kann, ist diese Eigenschaft auf Aufrufe der [IAddrBook::ResolveName](iaddrbook-resolvename.md) -Methode auf FALSE festgelegt. Um als eine IP-Adresse zu verstehen, muss der Anzeigename des nicht aufgelösten Eintrags im Format X@Y. Z, beispielsweise "pete@pinecone.com". 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> aus dem Internet standard-e-Mail-Konventionen für die Message-Objekten.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[PidTagAttachDataObject (kanonische Eigenschaft)](pidtagattachdataobject-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

