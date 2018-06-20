---
title: Kanonische PidTagMemberRights-Eigenschaft
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
ms.openlocfilehash: 2ffc6973d2670402ec8095120eea3db02f529d0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794601"
---
# <a name="pidtagmemberrights-canonical-property"></a>Kanonische PidTagMemberRights-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine Reihe von Bits an, die die Rechte von dieser Member in einem Ordner oder Postfach angegeben.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_MEMBER_RIGHTS  <br/> |
|Bezeichner:  <br/> |0x6673  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Steuerung des Zugriffs  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird von der [IExchangeModifyTable](iexchangemodifytableiunknown.md) -Schnittstelle zum Rechte eines Elements in einem Ordner zu definieren. Diese Rechte können angezeigt und geändert werden. Die folgenden Werte sind für diese Eigenschaft festgelegten Berechtigungen. 
  
frightsReadAny
  
> Member kann Nachrichten nicht gelesen.
    
frightsCreate
  
> Member kann Nachrichten erstellen.
    
frightsEditOwned
  
> Member kann alle Nachrichten, deren Besitzer der Benutzer bearbeiten.
    
frightsDeleteOwned
  
> Member kann alle Nachrichten, deren Besitzer der Benutzer löschen.
    
frightsEditAny
  
> Member kann eine beliebige Nachricht bearbeiten.
    
frightsDeleteAny
  
> Member kann eine beliebige Nachricht löschen.
    
frightsCreateSubfolder
  
> Member kann Unterordner für den Ordner erstellen.
    
frightsOwner
  
> Mitglied hat alle vorherigen Rechte für den Ordner.
    
frightsContact
  
> Member können Ihren Namen als den Kontakt für den Ordner angezeigt werden.
    
frightsVisible
  
> Member kann sehen, dass der Ordner vorhanden ist.
    
rightsNone
  
> Member verfügt nicht Rechte für den Ordner.
    
rightsReadOnly
  
> Member kann eine beliebige Nachricht im Ordner lesen.
    
rightsReadWrite
  
> Member kann aus lesen und Schreiben in eine beliebige Nachricht im Ordner.
    
rightsAll
  
> Mitglied hat alle vorherigen Rechte für den Ordner.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Ordner Vorgänge behandelt.
    
[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Behandelt das Abrufen von Ordner Berechtigungslisten, die auf dem Server gespeichert sind.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt die Methoden zum Verbinden mit und Postfächer als Stellvertreter und Interaktionen mit Nachrichten und Kalenderelemente konfigurieren, wenn sie im Auftrag eines anderen Benutzers agieren.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

