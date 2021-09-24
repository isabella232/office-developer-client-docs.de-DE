---
title: Kanonische PidTagDisplayType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1e48d31ade72639adfa5ea5f9d4d2e87a201b302
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550701"
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft enthält eine lange ganze Zahl, die die besondere Behandlung des Tabelleneintrags basierend auf seinem Typ erleichtert. Diese besondere Behandlung besteht in der Regel darin, ein Symbol oder ein anderes Anzeigeelement anzuzeigen, das dem Anzeigetyp zugeordnet ist. 
  
Diese Eigenschaft wird nicht in Ordnerinhaltstabellen verwendet. Clientanwendungen sollten die **eigenschaft PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) einer Nachricht und die entsprechende [IMAPIFormInfo-Schnittstelle](imapiforminfoimapiprop.md) verwenden, um die **Eigenschaften PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) und **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) für diese Nachricht abzurufen. 
  
Diese Eigenschaft kann genau einen der folgenden Werte haben:
  
DT_AGENT 
  
> Ein automatisierter Agent, z. B. "Quote-Of-The-Day" oder eine Wetterdiagrammanzeige.
    
DT_DISTLIST 
  
> Eine Verteilerliste.
    
DT_FOLDER 
  
> Zeigt das Standardordnersymbol neben dem Ordner an.
    
DT_FOLDER_LINK 
  
> Zeigt das Standard-Ordnerverknüpfungssymbol neben dem Ordner anstelle des Standardordnersymbols an.
    
DT_FOLDER_SPECIAL 
  
> Anzeigesymbol für einen Ordner mit anwendungsspezifischer Unterscheidung, z. B. einem speziellen Öffentlichen Ordnertyp.
    
DT_FORUM 
  
> Ein Forum, z. B. einBulletin-Board-Dienst oder ein öffentlicher oder freigegebener Ordner.
    
DT_GLOBAL 
  
> Ein globales Adressbuch.
    
DT_LOCAL 
  
> Ein lokales Adressbuch, das Sie mit einer kleinen Arbeitsgruppe teilen.
    
DT_MAILUSER 
  
> Ein typischer Messaging-Benutzer.
    
DT_MODIFIABLE 
  
> Modifizierbar; Der Container sollte auf der Benutzeroberfläche als modifizierbar gekennzeichnet werden.
    
DT_NOT_SPECIFIC 
  
> Entspricht keiner der anderen Einstellungen.
    
DT_ORGANIZATION 
  
> Ein spezieller Alias, der für eine große Gruppe definiert ist, z. B. Helpdesk- oder Buchhaltungs- oder Blut-Laufwerk-Coordinator.
    
DT_PRIVATE_DISTLIST 
  
> Eine private, persönlich verwaltete Verteilerliste.
    
DT_REMOTE_MAILUSER 
  
> Ein Empfänger, der bekannt ist, dass er von einem fremden oder Remotenachrichtensystem stammt.
    
DT_WAN 
  
> Ein Adressbuch für ein breites Netzwerk.
    
Adressbuchinhaltsverzeichnisse verwenden die Werte DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST und DT_REMOTE_MAILUSER. Adressbuchhierarchietabellen und einmalige Tabellen verwenden die Werte DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC und DT_WAN. Ordnerhierarchietabellen verwenden die Werte DT_FOLDER, DT_FOLDER_LINK und DT_FOLDER_SPECIAL. 
  
Wenn diese Eigenschaft nicht festgelegt ist, sollte der Client den für die Tabelle geeigneten Standardtyp annehmen, in der Regel DT_FOLDER, DT_LOCAL oder DT_MAILUSER. 
  
 **Hinweis** Alle nicht dokumentierten Werte sind für DIE MAPI reserviert. Clientanwendungen dürfen keine neuen Werte definieren und müssen darauf vorbereitet sein, mit einem undokumentierten Wert umzugehen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Adressbuchvorlagen zulässig sind.
    
[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> Aktiviert den Verzeichniszugriff.
    
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

