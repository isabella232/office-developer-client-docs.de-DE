---
title: PidTagResourceFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagResourceFlags
api_type:
- COM
ms.assetid: 69be9ad3-006a-459e-9cd4-eb3f609d71ad
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f2e9100993b02f165c58f60b81307b6b5d04c647
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563357"
---
# <a name="pidtagresourceflags-canonical-property"></a>PidTagResourceFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags für Nachrichtendienste und -anbieter.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RESOURCE_FLAGS  <br/> |
|Kennung:  <br/> |0x3009  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |ALLGEMEINE MAPI  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft beschreibt die Merkmale eines Nachrichtendiensts, eines Dienstanbieters oder eines Statusobjekts. Die Flags, die für diese Eigenschaft festgelegt sind, hängen vom Kontext ab. Beispielsweise sind einige Flags nur für Statusobjekte und andere Flags nur für Spalten in der Nachrichtendiensttabelle gültig. 
  
Die Flags bestehen aus drei Klassen: statisch, modifizierbar und dynamisch. Statische Flags werden von MAPI aus Daten in MAPISVC festgelegt. INF und nie geändert. Modifiierbare Flags werden von MAPI von MAPISVC festgelegt. INF, kann aber anschließend geändert werden. Dynamische Flags können mit MAPI-Methoden festgelegt und zurückgesetzt werden.
  
Für einen Nachrichtendienst kann in dieser Eigenschaft eines oder mehrere der folgenden Flags festgelegt werden:
  
SERVICE_CREATE_WITH_STORE 
  
> Reserviert. Nicht verwenden.
    
SERVICE_DEFAULT_STORE 
  
> Dynamische. Der Nachrichtendienst enthält den Standardspeicher. Es sollte eine Benutzeroberfläche angezeigt werden, die den Benutzer zur Bestätigung auffordert, bevor dieser Dienst gelöscht oder aus dem Profil verschoben wird. 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> Statische. Das Flag auf Dienstebene, das festgelegt werden sollte, um anzugeben, dass keiner der Anbieter im Nachrichtendienst verwendet werden kann, um eine Identität anzugeben. Entweder dieses Flag oder SERVICE_PRIMARY_IDENTITY sollte festgelegt werden, aber nicht beides.
    
SERVICE_PRIMARY_IDENTITY 
  
> Änderbaren. Der entsprechende Nachrichtendienst enthält den Anbieter, der für die primäre Identität für diese Sitzung verwendet wird. Verwenden Sie [IMsgServiceAdmin::SetPrimaryIdentity,](imsgserviceadmin-setprimaryidentity.md) um dieses Flag festzulegen. Entweder dieses Flag oder SERVICE_NO_PRIMARY_IDENTITY sollte festgelegt werden, aber nicht beides. 
    
SERVICE_SINGLE_COPY 
  
> Statische. Jeder Versuch, diesen Nachrichtendienst zu erstellen oder in ein Profil zu kopieren, in dem der Dienst bereits vorhanden ist, schlägt fehl. Zum Erstellen eines einzelnen Kopiernachrichtendiensts fügen Sie die **PR_RESOURCE_FLAGS-Eigenschaft** zum Abschnitt des Diensts in MAPISVC hinzu. INF, und legen Sie dieses Flag fest. 
    
Für einen Dienstanbieter kann ein oder mehrere der folgenden Flags in **PR_RESOURCE_FLAGS** festgelegt werden:
  
HOOK_INBOUND 
  
> Statische. Der Spooler-Hook muss eingehende Nachrichten verarbeiten.
    
HOOK_OUTBOUND 
  
> Statische. Der Spooler-Hook muss ausgehende Nachrichten verarbeiten. 
    
STATUS_DEFAULT_OUTBOUND 
  
> Änderbaren. Diese Identität sollte auf ausgehende Nachrichten angewendet werden, wenn das Profil mehrere Instanzen dieses Transportanbieters enthält. Dies kann passieren, wenn mehrere Instanzen eines einzelnen Transportanbieters im Profil angezeigt werden.
    
STATUS_DEFAULT_STORE 
  
> Änderbaren. Dieser Nachrichtenspeicher ist der Standardspeicher für das Profil. 
    
STATUS_NEED_IPM_TREE 
  
> Dynamische. Die Standardordner in diesem Nachrichtenspeicher, einschließlich des Stammordners für zwischenmenschliche Nachrichten (Interpersonal Message, IPM), wurden noch nicht überprüft. MapI legt dieses Kennzeichen fest und löscht es. 
    
STATUS_NO_DEFAULT_STORE 
  
> Statische. Dieser Nachrichtenspeicher kann nicht zum Standardnachrichtenspeicher für das Profil werden.
    
STATUS_NO_PRIMARY_IDENTITY 
  
> Statische. Dieser Anbieter stellt keine Identität in der Statuszeile bereit. Entweder dieses Flag oder STATUS_PRIMARY_IDENTITY muss festgelegt werden.
    
STATUS_OWN_STORE 
  
> Statische. Dieser Transportanbieter ist eng mit einem Nachrichtenspeicher verbunden und stellt die **Eigenschaft PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) in der Statuszeile bereit.
    
STATUS_PRIMARY_IDENTITY 
  
> Änderbaren. Dieser Anbieter stellt die primäre Identität für die Sitzung bereit. Der Eintragsbezeichner für das Objekt, das die Identität erhält, wird von [IMAPISession::QueryIdentity](imapisession-queryidentity.md)zurückgegeben. Entweder dieses Flag oder **STATUS_NO_PRIMARY_IDENTITY** muss festgelegt werden. 
    
STATUS_PRIMARY_STORE 
  
> Änderbaren. Dieser Nachrichtenspeicher soll verwendet werden, wenn sich eine Clientanwendung anmeldet. Nach dem Öffnen sollte dieser Speicher als Standardspeicher für das Profil festgelegt werden. 
    
STATUS_SECONDARY_STORE 
  
> Änderbaren. Dieser Nachrichtenspeicher wird verwendet, wenn der primäre Speicher nicht verfügbar ist, wenn sich eine Clientanwendung anmeldet. Nach dem Öffnen sollte dieser Speicher als Standardspeicher für das Profil festgelegt werden. 
    
STATUS_SIMPLE_STORE 
  
> Dynamische. Dieser Nachrichtenspeicher wird von der einfachen MAPI als Standardnachrichtenspeicher verwendet.
    
STATUS_TEMP_SECTION 
  
> Dynamische. Dieser Nachrichtenspeicher sollte nicht in der Nachrichtenspeichertabelle veröffentlicht werden und wird nach der Abmeldung aus dem Profil gelöscht. 
    
STATUS_XP_PREFER_LAST 
  
> Statische. Dieser Transport erwartet, dass der letzte Transport zum Senden einer Nachricht ausgewählt ist, wenn mehrere Transportanbieter in der Lage sind, die Nachricht zu übertragen.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[PidTagIdentityEntryId (kanonische Eigenschaft)](pidtagidentityentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

