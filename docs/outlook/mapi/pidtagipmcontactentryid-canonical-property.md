---
title: PidTagIpmContactEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagIpmContactEntryId
api_type:
- HeaderDef
ms.assetid: fccbbb15-dd08-4310-83d7-bf57eb3ed5de
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 040c39469329b9b3c894f2c98daf48741110a309
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600036"
---
# <a name="pidtagipmcontactentryid-canonical-property"></a>PidTagIpmContactEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die **EntryID** des Ordners Outlook Kontakte. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IPM_CONTACT_ENTRYID  <br/> |
|Kennung:  <br/> |0x36D1  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Ordner  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird im Ordner "Posteingang" und im Stammordner des Nachrichtenspeichers gespeichert. Gehen Sie wie folgt vor, um auf die Eigenschaft eines bestimmten Nachrichtenspeichers zuzugreifen: 
  
1. Suchen Sie zunächst nach der Eigenschaft im Ordner "Posteingang". Verwenden Sie **IMsgStore::GetReceiveFolder,** um einen Verweis auf die **EntryID** für den Posteingangsordner abzurufen. 
    
2. Wenn **IMsgStore::GetReceiveFolder** erfolgreich ist, verwenden Sie den Verweis auf die **EntryID** des Posteingangs und **IMsgStore::OpenEntry,** um den Posteingang zu öffnen und einen Verweis auf ein **IMAPIFolder** -Objekt abzurufen. 
    
3. Wenn **IMsgStore::OpenEntry** erfolgreich ist, verwenden Sie den zurückgegebenen Verweis auf das **IMAPIFolder-Objekt** und **IMAPIProp::GetProps,** um die gewünschte Eigenschaft abzurufen. 
    
4. Wenn schritt 1, 2 oder 3 fehlschlägt, suchen Sie nach der Eigenschaft im Stammordner. Verwenden Sie dazu **IMsgStore::OpenEntry,** das NULL für ** lpEntryID ** angibt, um den Stammordner des Nachrichtenspeichers zu öffnen und einen Verweis auf das **IMAPIFolder** -Objekt abzurufen. 
    
5. Wenn das Öffnen des Stammordners erfolgreich ist, verwenden Sie den zurückgegebenen Verweis auf das **IMAPIFolder-Objekt** und **IMAPIProp::GetProps,** um die gewünschte Eigenschaft abzurufen. 
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Erstellen und Suchen der speziellen Ordner in einem Postfach an.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Verbinden mit und Konfigurieren von Postfächern als Stellvertretungen und Interaktionen mit Nachrichten- und Kalenderobjekten an, wenn sie im Auftrag eines anderen Benutzers handeln.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

