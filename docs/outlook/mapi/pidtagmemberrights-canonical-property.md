---
title: PidTagMemberRights (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberRights
api_type:
- HeaderDef
ms.assetid: 3e526b93-1f64-41ea-b43c-5b03fe1c56ed
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dcbf8a323f5178a5a2e39d0963dd19415ab835bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342694"
---
# <a name="pidtagmemberrights-canonical-property"></a>PidTagMemberRights (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Gruppe von Bits, die die Rechte dieses Mitglieds für einen Ordner oder ein Postfach angegeben haben.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MEMBER_RIGHTS  <br/> |
|Kennung:  <br/> |0x6673  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Zugriffssteuerung  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird von der [IExchangeModifyTable-Schnittstelle](iexchangemodifytableiunknown.md) zum Definieren von Rechten eines Mitglieds in einem Ordner verwendet. Diese Rechte können angezeigt und geändert werden. Die folgenden Werte sind Rechte, die für diese Eigenschaft definiert sind. 
  
frightsReadAny
  
> Mitglied kann alle Nachrichten lesen.
    
frightsCreate
  
> Member kann Nachrichten erstellen.
    
frightsEditOwned
  
> Member kann alle Nachrichten bearbeiten, die im Besitz des Benutzers sind.
    
frightsDeleteOwned
  
> Member kann alle Nachrichten löschen, die im Besitz des Benutzers sind.
    
frightsEditAny
  
> Member kann jede Nachricht bearbeiten.
    
frightsDeleteAny
  
> Member kann jede Nachricht löschen.
    
frightsCreateSubfolder
  
> Member kann Unterordner für den Ordner erstellen.
    
frightsOwner
  
> Das Mitglied verfügt über alle vorherigen Rechte für den Ordner.
    
frightsContact
  
> Der Name des Mitglieds kann als Kontakt im Ordner angezeigt werden.
    
frightsVisible
  
> Das Mitglied kann sehen, dass der Ordner vorhanden ist.
    
rightsNone
  
> Member hat keine Rechte für den Ordner.
    
rightsReadOnly
  
> Mitglied kann jede Nachricht im Ordner lesen.
    
rightsReadWrite
  
> Member kann aus einer beliebigen Nachricht im Ordner lesen und in diese schreiben.
    
rightsAll
  
> Das Mitglied verfügt über alle vorherigen Rechte für den Ordner.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Verarbeitet Ordnervorgänge.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Behandelt das Abrufen von Ordnerberechtigungslisten, die auf dem Server gespeichert sind.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Herstellen und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten- und Kalenderelementen an, wenn sie im Auftrag eines anderen Benutzers agieren.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

