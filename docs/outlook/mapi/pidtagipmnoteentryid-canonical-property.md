---
title: PidTagIpmNoteEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmNoteEntryId
api_type:
- HeaderDef
ms.assetid: c003f7b9-b0cd-4656-98fa-3466fda6832c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3d465bfeb30d4f2964254b1d1f524f964fde7239
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327872"
---
# <a name="pidtagipmnoteentryid-canonical-property"></a>PidTagIpmNoteEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die **EntryID** des Outlook Notes-Ordners. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IPM_NOTE_ENTRYID  <br/> |
|Kennung:  <br/> |0x36D3  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Ordner  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird im Ordner Posteingang sowie im Stammordner des Nachrichtenspeichers gespeichert. Gehen Sie wie folgt vor, um auf die Eigenschaft in einem bestimmten Nachrichtenspeicher zu zugreifen: 
  
1. Suchen Sie zunächst im Ordner Posteingang nach der Eigenschaft. Verwenden [Sie IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) um einen Verweis auf die **EntryID** für den Posteingangsordner zu erhalten. 
    
2. Wenn ** IMsgStore::GetReceiveFolder ** erfolgreich ist, verwenden Sie den Verweis auf die **EntryID** des Posteingangs und [IMsgStore::OpenEntry,](imsgstore-openentry.md) um den Posteingang zu öffnen und einen Verweis auf ein **IMAPIFolder-Objekt** zu erhalten. 
    
3. Wenn **IMsgStore::OpenEntry** erfolgreich ist, verwenden Sie den zurückgegebenen Verweis auf das **IMAPIFolder-Objekt** und [IMAPIProp::GetProps,](imapiprop-getprops.md) um die gewünschte Eigenschaft zu erhalten. 
    
4. Wenn in Schritt 1, 2 oder 3 ein Fehler auftritt, suchen Sie im Stammordner nach der Eigenschaft. Verwenden Sie **dazu IMsgStore::OpenEntry,** und geben Sie NULL für **lpEntryID** an, um den Stammordner des Nachrichtenspeichers zu öffnen und einen Verweis auf das **IMAPIFolder-Objekt** zu erhalten. 
    
5. Wenn das Öffnen des Stammordners erfolgreich ist, verwenden Sie den zurückgegebenen Verweis auf das **IMAPIFolder-Objekt** und **IMAPIProp::GetProps,** um die gewünschte Eigenschaft zu erhalten. 
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Erstellen und Suchen der speziellen Ordner in einem Postfach an.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Verbinden und Konfigurieren von Postfächern als Stellvertretung sowie Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers agieren.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

