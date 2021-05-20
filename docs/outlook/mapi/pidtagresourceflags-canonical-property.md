---
title: PidTagResourceFlags (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2fb9eed0beaf7269ac90a021dae650355484ebc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436230"
---
# <a name="pidtagresourceflags-canonical-property"></a>PidTagResourceFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags für Nachrichtendienste und Anbieter.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RESOURCE_FLAGS  <br/> |
|Kennung:  <br/> |0x3009  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI allgemein  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft beschreibt die Merkmale eines Nachrichtendiensts, eines Dienstanbieters oder eines Statusobjekts. Die für diese Eigenschaft festgelegten Flags hängen vom Kontext ab. Einige Flags sind beispielsweise nur für Statusobjekte und andere Flags nur für Spalten in der Nachrichtendiensttabelle gültig. 
  
Die Flags sind aus drei Klassen: statisch, veränderbar und dynamisch. Statische Flags werden von MAPI aus Daten in MAPISVC festgelegt. INF und nie geändert. Modifizierbare Flags werden von MAPI aus MAPISVC festgelegt. INF, kann aber anschließend geändert werden. Dynamische Flags können mit MAPI-Methoden festgelegt und zurückgesetzt werden.
  
Für einen Nachrichtendienst können in dieser Eigenschaft mindestens eines der folgenden Kennzeichen festgelegt werden:
  
SERVICE_CREATE_WITH_STORE 
  
> Reserviert. Nicht verwenden.
    
SERVICE_DEFAULT_STORE 
  
> Dynamisch. Der Nachrichtendienst enthält den Standardspeicher. Eine Benutzeroberfläche sollte angezeigt werden, in der der Benutzer zur Bestätigung aufgefordert wird, bevor dieser Dienst gelöscht oder aus dem Profil gelöscht wird. 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> Statisch. Das Servicelevel-Flag, das festgelegt werden soll, um anzugeben, dass keiner der Anbieter im Nachrichtendienst zum Angeben einer Identität verwendet werden kann. Entweder dieses Flag oder SERVICE_PRIMARY_IDENTITY sollte festgelegt werden, aber nicht beides.
    
SERVICE_PRIMARY_IDENTITY 
  
> Modifiable. Der entsprechende Nachrichtendienst enthält den Anbieter, der für die primäre Identität für diese Sitzung verwendet wird. Verwenden [Sie IMsgServiceAdmin::SetPrimaryIdentity,](imsgserviceadmin-setprimaryidentity.md) um dieses Flag zu setzen. Entweder dieses Flag oder SERVICE_NO_PRIMARY_IDENTITY sollte festgelegt werden, aber nicht beides. 
    
SERVICE_SINGLE_COPY 
  
> Statisch. Bei jedem Versuch, diesen Nachrichtendienst in ein Profil zu erstellen oder zu kopieren, in dem der Dienst bereits vorhanden ist, wird ein Fehler angezeigt. Fügen Sie zum Erstellen eines einzelnen Kopiernachrichtendiensts **die PR_RESOURCE_FLAGS** dem Abschnitt des Diensts in MAPISVC hinzu. INF, und legen Sie dieses Flag ein. 
    
Für einen Dienstanbieter können mindestens eines der folgenden Flags **in** der PR_RESOURCE_FLAGS:
  
HOOK_INBOUND 
  
> Statisch. Der Spooler-Hook muss eingehende Nachrichten verarbeiten.
    
HOOK_OUTBOUND 
  
> Statisch. Der Spooler-Hook muss ausgehende Nachrichten verarbeiten. 
    
STATUS_DEFAULT_OUTBOUND 
  
> Modifiable. Diese Identität sollte auf ausgehende Nachrichten angewendet werden, wenn das Profil mehrere Instanzen dieses Transportanbieters enthält. Dies kann passieren, wenn mehrere Instanzen eines einzelnen Transportanbieters im Profil angezeigt werden.
    
STATUS_DEFAULT_STORE 
  
> Modifiable. Dieser Nachrichtenspeicher ist der Standardspeicher für das Profil. 
    
STATUS_NEED_IPM_TREE 
  
> Dynamisch. Die Standardordner in diesem Nachrichtenspeicher, einschließlich des Stammordners für zwischenperson message (IPM), wurden noch nicht überprüft. MAPI legt dieses Flag fest und entfernt es. 
    
STATUS_NO_DEFAULT_STORE 
  
> Statisch. Dieser Nachrichtenspeicher kann nicht zum Standardnachrichtenspeicher für das Profil werden.
    
STATUS_NO_PRIMARY_IDENTITY 
  
> Statisch. Dieser Anbieter stellt keine Identität in seiner Statuszeile zur. Entweder dieses Flag oder STATUS_PRIMARY_IDENTITY muss festgelegt werden.
    
STATUS_OWN_STORE 
  
> Statisch. Dieser Transportanbieter ist eng mit einem Nachrichtenspeicher gekoppelt und bietet die **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) -Eigenschaft in der Statuszeile an.
    
STATUS_PRIMARY_IDENTITY 
  
> Modifiable. Dieser Anbieter gibt die primäre Identität für die Sitzung an. der Eintragsbezeichner für das Objekt, das die Identität aus [der IMAPISession::QueryIdentity zurückerkennt.](imapisession-queryidentity.md) Entweder dieses Flag **oder STATUS_NO_PRIMARY_IDENTITY** muss festgelegt werden. 
    
STATUS_PRIMARY_STORE 
  
> Modifiable. Dieser Nachrichtenspeicher soll verwendet werden, wenn sich eine Clientanwendung anmeldet. Nach dem Öffnen sollte dieser Speicher als Standardspeicher für das Profil festgelegt werden. 
    
STATUS_SECONDARY_STORE 
  
> Modifiable. Dieser Nachrichtenspeicher soll verwendet werden, wenn der primäre Speicher nicht verfügbar ist, wenn sich eine Clientanwendung anmeldet. Nach dem Öffnen sollte dieser Speicher als Standardspeicher für das Profil festgelegt werden. 
    
STATUS_SIMPLE_STORE 
  
> Dynamisch. Dieser Nachrichtenspeicher wird von simple MAPI als Standardnachrichtenspeicher verwendet.
    
STATUS_TEMP_SECTION 
  
> Dynamisch. Dieser Nachrichtenspeicher sollte nicht in der Nachrichtenspeichertabelle veröffentlicht werden und nach dem Abmelden aus dem Profil gelöscht werden. 
    
STATUS_XP_PREFER_LAST 
  
> Statisch. Dieser Transport ist der letzte Transport, der ausgewählt wurde, um eine Nachricht zu senden, wenn mehrere Transportanbieter die Nachricht übertragen können.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[PidTagIdentityEntryId (kanonische Eigenschaft)](pidtagidentityentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

