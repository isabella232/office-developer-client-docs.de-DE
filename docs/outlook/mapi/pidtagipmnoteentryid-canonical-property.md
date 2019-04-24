---
title: Kanonische Pidtagipmnoteentryid (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3d465bfeb30d4f2964254b1d1f524f964fde7239
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327872"
---
# <a name="pidtagipmnoteentryid-canonical-property"></a>Kanonische Pidtagipmnoteentryid (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die **Eintrags** -Nr. des Outlook-Notes-Ordners. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IPM_NOTE_ENTRYID  <br/> |
|Kennung:  <br/> |0x36D3  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Ordner  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird im Ordner Posteingang und im Stammordner des Nachrichtenspeichers gespeichert. Gehen Sie folgendermaßen vor, um auf die Eigenschaft in einem bestimmten Nachrichtenspeicher zuzugreifen: 
  
1. Suchen Sie zunächst nach der-Eigenschaft im Ordner Posteingang. Verwenden Sie [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) , um einen Verweis auf die **Eintrags** -Nr. für den Posteingangsordner abzurufen. 
    
2. Wenn * * IMsgStore:: GetReceiveFolder * * erfolgreich ist, verwenden Sie den Verweis auf die **Eintrags** -und [IMsgStore:: OpenEntry](imsgstore-openentry.md) , um den Posteingang zu öffnen und einen Verweis auf ein **IMAPIFolder** -Objekt abzurufen. 
    
3. Wenn **IMsgStore:: OpenEntry** erfolgreich ist, verwenden Sie den zurückgegebenen Verweis auf das **IMAPIFolder** -Objekt und [IMAPIProp::](imapiprop-getprops.md) GetProps, um die gewünschte Eigenschaft abzurufen. 
    
4. Wenn Schritt 1, 2 oder 3 fehlschlägt, suchen Sie nach der Eigenschaft im Stammordner. Zu diesem Zweck verwenden Sie **IMsgStore:: OpenEntry**, angeben von NULL für **lpEntryID**, um den Stammordner des Nachrichtenspeichers zu öffnen und einen Verweis auf das **IMAPIFolder** -Objekt abzurufen. 
    
5. Wenn das Öffnen des Stammordners erfolgreich ist, verwenden Sie den zurückgegebenen Verweis auf das **IMAPIFolder** -Objekt und **IMAPIProp::** GetProps, um die gewünschte Eigenschaft abzurufen. 
    
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Erstellen und suchen der speziellen Ordner in einem Postfach an.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Gibt Methoden zum Herstellen einer Verbindung mit und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten-und Kalenderobjekten an, wenn Sie im Auftrag eines anderen Benutzers agieren.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

