---
title: Kanonische PidTagDisplayType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: da26fd2a8643817cf60adbfa6f4e85da345b875c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360781"
---
# <a name="pidtagdisplaytype-canonical-property"></a>Kanonische PidTagDisplayType-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert, der zum Zuordnen eines Symbols zu einer bestimmten Zeile einer Tabelle verwendet wird. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISPLAY_TYPE  <br/> |
|Kennung:  <br/> |0x3900  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält eine lange ganze Zahl, die eine spezielle Behandlung des Tabelleneintrags basierend auf dem Typ ermöglicht. Diese spezielle Behandlung besteht in der Regel darin, ein Symbol oder ein anderes Anzeigeelement anzuzeigen, das dem Anzeigetyp zugeordnet ist. 
  
Diese Eigenschaft wird nicht in Ordnerinhaltstabellen verwendet. Client Anwendungen sollten die **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft einer Nachricht und die entsprechende [IMAPIFormInfo](imapiforminfoimapiprop.md) -Schnittstelle verwenden, um die **PR_ICON** ([pidtagicon (](pidtagicon-canonical-property.md)) und **PR_MINI_ICON** abzurufen ([ Pidtagminiicon (](pidtagminiicon-canonical-property.md))-Eigenschaften für diese Nachricht. 
  
Diese Eigenschaft kann genau einen der folgenden Werte haben:
  
DT_AGENT 
  
> Ein automatisierter Agent, wie beispielsweise "Quote-of-the-Day"-oder eine Wetter Diagrammanzeige.
    
DT_DISTLIST 
  
> Eine Verteilerliste.
    
DT_FOLDER 
  
> Standardordner Symbol neben Ordner anzeigen
    
DT_FOLDER_LINK 
  
> Symbol für Standardordner Verknüpfung neben Ordner anstelle des Standardordner Symbols anzeigen.
    
DT_FOLDER_SPECIAL 
  
> Anzeigesymbol für einen Ordner mit anwendungsspezifischer Unterscheidung, beispielsweise einen speziellen öffentlichen Ordnertyp.
    
DT_FORUM 
  
> Ein Forum, beispielsweise ein Bulletin Board-Dienst oder ein öffentlicher oder freigegebener Ordner.
    
DT_GLOBAL 
  
> Ein globales Adressbuch.
    
DT_LOCAL 
  
> Ein lokales Adressbuch, das Sie für eine kleine Arbeitsgruppe freigeben.
    
DT_MAILUSER 
  
> Ein typischer Messagingbenutzer.
    
DT_MODIFIABLE 
  
> Änderbaren der Container sollte in der Benutzeroberfläche als veränderbar gekennzeichnet werden.
    
DT_NOT_SPECIFIC 
  
> Stimmt mit keiner der anderen Einstellungen überein.
    
DT_ORGANIZATION 
  
> Ein spezieller Alias, der für eine umfangreiche Gruppe definiert wurde, beispielsweise Helpdesk, Accounting oder Blood-Drive Coordinator.
    
DT_PRIVATE_DISTLIST 
  
> Eine private, persönlich verwaltete Verteilerliste.
    
DT_REMOTE_MAILUSER 
  
> Ein Empfänger, der bekanntermaßen von einem fremd-oder Remote Messagingsystem stammt.
    
DT_WAN 
  
> Ein Wide Area Network-Adressbuch.
    
In den Adressbuch Inhaltstabellen werden die Werte DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST und DT_REMOTE_MAILUSER verwendet. Adressbuch-Hierarchietabellen und einmalige Tabellen verwenden Sie die Werte DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC und DT_WAN. Ordner Hierarchietabellen verwenden die DT_FOLDER-, DT_FOLDER_LINK-und DT_FOLDER_SPECIAL-Werte. 
  
Wenn diese Eigenschaft nicht festgelegt ist, sollte der Client den für die Tabelle geeigneten Standardtyp annehmen, in der Regel DT_FOLDER, DT_LOCAL oder DT_MAILUSER. 
  
 **Hinweis** Alle nicht dokumentierten Werte sind für MAPI reserviert. Client Anwendungen dürfen keine neuen Werte definieren und müssen auf den Umgang mit einem nicht dokumentierten Wert vorbereitet sein. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Adressbuchvorlagen zulässig sind.
    
[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> Aktiviert den Verzeichniszugriff.
    
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

