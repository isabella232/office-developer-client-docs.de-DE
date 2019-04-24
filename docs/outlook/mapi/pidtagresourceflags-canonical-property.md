---
title: Kanonische Pidtagresourceflags (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceFlags
api_type:
- COM
ms.assetid: 69be9ad3-006a-459e-9cd4-eb3f609d71ad
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2fb9eed0beaf7269ac90a021dae650355484ebc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330184"
---
# <a name="pidtagresourceflags-canonical-property"></a>Kanonische Pidtagresourceflags (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske von Flags für Nachrichtendienste und Anbieter.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RESOURCE_FLAGS  <br/> |
|Kennung:  <br/> |0x3009  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI allgemein  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft beschreibt die Merkmale eines Nachrichtendiensts, eines Dienstanbieters oder eines Status Objekts. Die für diese Eigenschaft festgelegten Flags hängen vom jeweiligen Kontext ab. Beispielsweise sind einige Flags nur für Statusobjekte und andere Flags nur für Spalten in der Nachrichtendienst Tabelle gültig. 
  
Die Flags bestehen aus drei Klassen: statisch, änderbar und dynamisch. Statische Flags werden von Daten in MAPISVC von MAPI festgelegt. INF und nie geändert. Veränderbare Flags werden von MAPI von MAPISVC festgelegt. INF kann aber nachträglich geändert werden. Dynamische Kennzeichnungen können durch MAPI-Methoden festgelegt und zurückgesetzt werden.
  
Bei einem Nachrichtendienst können eine oder mehrere der folgenden Flags in dieser Eigenschaft festgelegt werden:
  
SERVICE_CREATE_WITH_STORE 
  
> Reserviert. Nicht verwenden.
    
SERVICE_DEFAULT_STORE 
  
> Dynamische. Der Nachrichtendienst enthält den Standardspeicher. Es sollte eine Benutzeroberfläche angezeigt werden, in der der Benutzer zur Bestätigung aufgefordert wird, bevor dieser Dienst aus dem Profil gelöscht oder entfernt wird. 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> Statische. Das Dienst Level-Flag, das festgelegt werden sollte, um anzugeben, dass keiner der Anbieter im Nachrichtendienst zur Bereitstellung einer Identität verwendet werden kann. Entweder dieses Flag oder SERVICE_PRIMARY_IDENTITY sollte festgelegt werden, aber nicht beides.
    
SERVICE_PRIMARY_IDENTITY 
  
> Änderbaren. Der entsprechende Nachrichtendienst enthält den Anbieter, der für die primäre Identität für diese Sitzung verwendet wird. Verwenden Sie [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) , um dieses Flag festzulegen. Entweder dieses Flag oder SERVICE_NO_PRIMARY_IDENTITY sollte festgelegt werden, aber nicht beides. 
    
SERVICE_SINGLE_COPY 
  
> Statische. Jeder Versuch, diesen Nachrichtendienst in ein Profil zu erstellen oder zu kopieren, in dem der Dienst bereits vorhanden ist, schlägt fehl. So erstellen Sie einen Einzelkopiecluster-Dienst fügen Sie die **PR_RESOURCE_FLAGS** -Eigenschaft zum Abschnitt des Diensts in Mapisvc hinzu. INF, und legen Sie dieses Flag fest. 
    
Bei einem Dienstanbieter kann eine oder mehrere der folgenden Flags in **PR_RESOURCE_FLAGS**festgelegt werden:
  
HOOK_INBOUND 
  
> Statische. Der Spooler-Hook muss eingehende Nachrichten verarbeiten.
    
HOOK_OUTBOUND 
  
> Statische. Der Spooler-Hook muss ausgehende Nachrichten verarbeiten. 
    
STATUS_DEFAULT_OUTBOUND 
  
> Änderbaren. Diese Identität sollte auf ausgehende Nachrichten angewendet werden, wenn das Profil mehrere Instanzen dieses Transportanbieters enthält. Dies kann passieren, wenn mehrere Instanzen eines einzelnen Transportanbieters im Profil angezeigt werden.
    
STATUS_DEFAULT_STORE 
  
> Änderbaren. Dieser Nachrichtenspeicher ist der Standardspeicher für das Profil. 
    
STATUS_NEED_IPM_TREE 
  
> Dynamische. Die Standardordner in diesem Nachrichtenspeicher, einschließlich des Stammordners für die zwischenmenschlichen Nachrichten (IPM), wurden noch nicht überprüft. Das Flag wird von MAPI festgelegt und gelöscht. 
    
STATUS_NO_DEFAULT_STORE 
  
> Statische. Dieser Nachrichtenspeicher kann nicht zum Standardnachrichtenspeicher für das Profil werden.
    
STATUS_NO_PRIMARY_IDENTITY 
  
> Statische. Dieser Anbieter liefert keine Identität in der Statuszeile. Entweder dieses Flag oder STATUS_PRIMARY_IDENTITY muss festgelegt werden.
    
STATUS_OWN_STORE 
  
> Statische. Dieser Transportanbieter ist eng mit einem Nachrichtenspeicher gekoppelt und liefert die **PR_OWN_STORE_ENTRYID** ([pidtagownstoreentryid (](pidtagownstoreentryid-canonical-property.md))-Eigenschaft in der Statuszeile.
    
STATUS_PRIMARY_IDENTITY 
  
> Änderbaren. Dieser Anbieter liefert die primäre Identität für die Sitzung; die Eintrags-ID für das Objekt, das die Identität eingibt, wird von [IMAPISession:: QueryIdentity](imapisession-queryidentity.md)zurückgegeben. Entweder dieses Flag oder **STATUS_NO_PRIMARY_IDENTITY** muss festgelegt werden. 
    
STATUS_PRIMARY_STORE 
  
> Änderbaren. Dieser Nachrichtenspeicher soll verwendet werden, wenn sich eine Clientanwendung anmeldet. Nach dem Öffnen sollte dieser Speicher als Standardspeicher für das Profil festgelegt werden. 
    
STATUS_SECONDARY_STORE 
  
> Änderbaren. Dieser Nachrichtenspeicher soll verwendet werden, wenn der primäre Speicher nicht verfügbar ist, wenn sich eine Clientanwendung anmeldet. Nach dem Öffnen sollte dieser Speicher als Standardspeicher für das Profil festgelegt werden. 
    
STATUS_SIMPLE_STORE 
  
> Dynamische. Dieser Nachrichtenspeicher wird von Simple MAPI als Standardnachrichtenspeicher verwendet.
    
STATUS_TEMP_SECTION 
  
> Dynamische. Dieser Nachrichtenspeicher sollte nicht in der Nachrichtenspeichertabelle veröffentlicht werden und wird nach der Abmeldung aus dem Profil gelöscht. 
    
STATUS_XP_PREFER_LAST 
  
> Statische. Dieser Transport erwartet, dass er der letzte Transport ist, der zum Senden einer Nachricht ausgewählt wurde, wenn mehrere Transportanbieter die Nachricht übertragen können.
    
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[Kanonische Pidtagidentityentryid (-Eigenschaft](pidtagidentityentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

