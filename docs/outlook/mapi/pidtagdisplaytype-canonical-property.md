---
title: PidTagDisplayType (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5b067b3bc38df978cd0f4c52beb37579619edc24
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583512"
---
# <a name="pidtagdisplaytype-canonical-property"></a>PidTagDisplayType (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält einen Wert zum Verknüpfen eines Symbols mit einer bestimmten Zeile einer Tabelle verwendet. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DISPLAY_TYPE  <br/> |
|Kennung:  <br/> |0x3900  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Adressbuch  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft enthält eine lange Ganzzahl, die eine besondere Behandlung des Eintrags Tabelle basierend auf dieses Typs vereinfacht. Diese besondere Behandlung umfasst in der Regel ein Symbol oder andere Display-Element, den Anzeigetyp zugeordnete anzeigen. 
  
Diese Eigenschaft wird nicht im Ordner Inhalt Tabellen verwendet. Clientanwendungen sollte einer Meldung **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft und entsprechende [IMAPIFormInfo](imapiforminfoimapiprop.md) -Schnittstelle verwenden, um die **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) und **PR_MINI_ICON** ([ zu erhalten PidTagMiniIcon](pidtagminiicon-canonical-property.md)) Eigenschaften für diese Nachricht. 
  
Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:
  
DT_AGENT 
  
> Agent automatisierte wie Angebot des Tages oder eine Diagrammanzeige Wetter.
    
DT_DISTLIST 
  
> Eine Verteilerliste.
    
DT_FOLDER 
  
> Standard-Ordnersymbol neben der Ordner anzeigen.
    
DT_FOLDER_LINK 
  
> Zeigt Ordner Link Standardsymbol neben der Ordner, sondern das Standardsymbol für Ordner.
    
DT_FOLDER_SPECIAL 
  
> Zeigt das Symbol für einen Ordner mit einer anwendungsspezifischen Unterschied, wie etwa eine besondere Art des öffentlichen Ordners.
    
DT_FORUM 
  
> Foren, wie ein Bulletin Board-Dienst oder ein öffentlicher oder freigegebener Ordner.
    
DT_GLOBAL 
  
> Ein globales Adressbuch.
    
DT_LOCAL 
  
> Eine lokale Adressbuch, das für eine kleine Arbeitsgruppe freigegeben.
    
DT_MAILUSER 
  
> Normaler Benutzer messaging.
    
DT_MODIFIABLE 
  
> Änderbare; der Container sollte in der Benutzeroberfläche als änderbare gekennzeichnet werden.
    
DT_NOT_SPECIFIC 
  
> Stimmt mit keinem der anderen Einstellungen überein.
    
DT_ORGANIZATION 
  
> Eine spezielle Alias für eine große Gruppe wie Helpdesk, Buchhaltung oder Blut Laufwerk Coordinator definiert ist.
    
DT_PRIVATE_DISTLIST 
  
> Eine Private, persönlich verwaltet Verteilerliste.
    
DT_REMOTE_MAILUSER 
  
> Ein Empfänger bekanntermaßen aus einem fremden oder remote-messaging-System.
    
DT_WAN 
  
> Der Adressbuch eines WAN-Netzwerk.
    
Address Book Inhalt Tabellen verwenden Sie die Werte DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST und DT_REMOTE_MAILUSER. Verwenden Sie die Werte DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC und DT_WAN, Address Book Hierarchietabellen und einmaligen Tabellen. Ordner Hierarchietabellen verwenden Sie die Werte DT_FOLDER, DT_FOLDER_LINK und DT_FOLDER_SPECIAL. 
  
Wenn diese Eigenschaft nicht festgelegt ist, sollte der Client den Standardtyp für die Tabelle, in der Regel DT_FOLDER, DT_LOCAL oder DT_MAILUSER geeignet annehmen. 
  
 **Hinweis** Alle Werte, die nicht dokumentiert sind für die MAPI reserviert. Clientanwendungen dürfen Sie keine neue Werte definieren und für den Umgang mit eine nicht dokumentierte Wert vorbereitet sein. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Address Book Vorlagen zulässig sind.
    
[[MS-OXLDAP]](http://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> Verzeichniszugriff wird aktiviert.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

