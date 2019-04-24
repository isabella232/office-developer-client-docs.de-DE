---
title: Kanonische Pidtagmemberrights (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dcbf8a323f5178a5a2e39d0963dd19415ab835bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342694"
---
# <a name="pidtagmemberrights-canonical-property"></a>Kanonische Pidtagmemberrights (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Reihe von Bits, die die Rechte dieses Members für einen Ordner oder ein Postfach angegeben haben.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MEMBER_RIGHTS  <br/> |
|Kennung:  <br/> |0x6673  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Zugriffssteuerung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird von der [IExchangeModifyTable](iexchangemodifytableiunknown.md) -Schnittstelle verwendet, um die Rechte eines Members für einen Ordner zu definieren. Diese Rechte können angezeigt und geändert werden. Die folgenden Werte sind für diese Eigenschaft definierte Rechte. 
  
frightsReadAny
  
> Mitglieder können alle Nachrichten lesen.
    
frightsCreate
  
> Mitglied kann Nachrichten erstellen.
    
frightsEditOwned
  
> Mitglieder können alle Nachrichten bearbeiten, die dem Benutzer gehören.
    
frightsDeleteOwned
  
> Das Mitglied kann alle Nachrichten löschen, die dem Benutzer gehören.
    
frightsEditAny
  
> Mitglied kann jede Nachricht bearbeiten.
    
frightsDeleteAny
  
> Mitglied kann jede Nachricht löschen.
    
frightsCreateSubfolder
  
> Mitglied kann Unterordner für den Ordner erstellen.
    
frightsOwner
  
> Mitglied verfügt über alle vorherigen Rechte für den Ordner.
    
Berechtigung frightsContact
  
> Member kann Ihren Namen als Kontakt im Ordner angezeigt werden.
    
frightsVisible umgewandelt
  
> Mitglied kann sehen, dass der Ordner vorhanden ist.
    
rightsNone
  
> Member verfügt nicht über Rechte für den Ordner.
    
rightsReadOnly
  
> Mitglied kann alle Nachrichten im Ordner lesen.
    
rightsReadWrite
  
> Mitglied kann aus einer beliebigen Nachricht im Ordner lesen und diese schreiben.
    
rightsAll
  
> Mitglied verfügt über alle vorherigen Rechte für den Ordner.
    
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Behandelt Ordner Vorgänge.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Behandelt das Abrufen von Ordner Berechtigungslisten, die auf dem Server gespeichert sind.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Herstellen einer Verbindung mit und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten-und Kalenderelementen an, wenn Sie im Auftrag eines anderen Benutzers agieren.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

