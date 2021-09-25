---
title: PidTagMemberRights (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMemberRights
api_type:
- HeaderDef
ms.assetid: 3e526b93-1f64-41ea-b43c-5b03fe1c56ed
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b2adbd44107b07ac73e04bb7dbe2b3d87fae4bbf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595203"
---
# <a name="pidtagmemberrights-canonical-property"></a>PidTagMemberRights (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Reihe von Bits, die die Rechte dieses Mitglieds für einen Ordner oder ein Postfach angegeben haben.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MEMBER_RIGHTS  <br/> |
|Kennung:  <br/> |0x6673  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Zugriffskontrolle  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird von der [IExchangeModifyTable-Schnittstelle](iexchangemodifytableiunknown.md) zum Definieren der Rechte eines Mitglieds in einem Ordner verwendet. Diese Rechte können angezeigt und geändert werden. Die folgenden Werte sind für diese Eigenschaft definierte Rechte. 
  
frightsReadAny
  
> Member kann alle Nachrichten lesen.
    
frightsCreate
  
> Ein Mitglied kann Nachrichten erstellen.
    
frightsEditOwned
  
> Ein Mitglied kann alle Nachrichten bearbeiten, die dem Benutzer gehören.
    
frightsDeleteOwned
  
> Ein Mitglied kann alle Nachrichten löschen, die dem Benutzer gehören.
    
frightsEditAny
  
> Ein Mitglied kann eine beliebige Nachricht bearbeiten.
    
frightsDeleteAny
  
> Ein Mitglied kann eine beliebige Nachricht löschen.
    
frightsCreateSubfolder
  
> Member kann Unterordner für den Ordner erstellen.
    
frightsOwner
  
> Member verfügt über alle vorherigen Rechte für den Ordner.
    
frightsContact
  
> Member kann Ihren Namen als Kontakt im Ordner anzeigen lassen.
    
frightsVisible
  
> Member kann sehen, dass der Ordner vorhanden ist.
    
rightsNone
  
> Member hat keine Rechte für den Ordner.
    
rightsReadOnly
  
> Ein Mitglied kann eine beliebige Nachricht im Ordner lesen.
    
rightsReadWrite
  
> Member kann aus einer beliebigen Nachricht im Ordner lesen und in diese schreiben.
    
rightsAll
  
> Member verfügt über alle vorherigen Rechte für den Ordner.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Behandelt Ordnervorgänge.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Behandelt den Abruf von Ordnerberechtigungslisten, die auf dem Server gespeichert sind.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Verbinden mit und Konfigurieren von Postfächern als Stellvertretungen und Interaktionen mit Nachrichten- und Kalenderelementen an, wenn sie im Auftrag eines anderen Benutzers handeln.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

