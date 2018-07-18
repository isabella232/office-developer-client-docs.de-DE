---
title: PidLidFlagRequest (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: df2e474206559dadf250bdf9a078c69da61187c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793597"
---
# <a name="pidlidflagrequest-canonical-property"></a>PidLidFlagRequest (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Den Status der einer Besprechungsanfrage darstellt.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidRequest  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008530  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Kennzeichnen von  <br/> |
   
## <a name="remarks"></a>Bemerkungen

In Microsoft Office Outlook ist eine Besprechungsanfrage ein Terminelement.
  
Diese Eigenschaft enthält Benutzer festzulegen Text ein, um das Flag zugeordnet werden und festgelegt werden soll, wenn das Objekt "Message" gekennzeichnet oder abgeschlossen ist, jedoch nicht für ein Objekt bezüglich Besprechungen vorhanden sein. Clients können nicht für diese Eigenschaft unterstützen und in diese schreiben immer "Nachverfolgung" (übersetzte Sprache des Benutzers, falls zutreffend) als Wert für die Zeichenfolge, wenn diese Eigenschaft festgelegt werden soll. Diese Eigenschaft sollte bedingt basierend auf den Werten der **DispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) und **DispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) Eigenschaften ignoriert werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

