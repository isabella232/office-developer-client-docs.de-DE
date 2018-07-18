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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dae917b3e536aee5f24879edc3ccf0736e7c9f34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794976"
---
# <a name="pidtagresourceflags-canonical-property"></a>PidTagResourceFlags (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine Bitmaske aus Flags für die Message-Dienste und -Anbieter.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_RESOURCE_FLAGS  <br/> |
|Bezeichner:  <br/> |0x3009  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine MAPI  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft beschreibt die Merkmale eines Diensts Nachricht, einem Dienstanbieter oder Status-Objekts. Die Kennzeichen, die für diese Eigenschaft festgelegt sind, hängt von dessen Kontext ab. Beispielsweise sind einige Kennzeichen gilt nur für Objekte der Status und anderen Flags nur für Spalten in der Tabelle der Dienste. 
  
Die Flags sind drei Klassen: statische, änderbare und dynamische. Statische Flags werden anhand von Daten in MAPISVC MAPI festgelegt. INF-Datei und nicht mehr verändert. Änderbare Flags werden von MAPI aus MAPISVC festgelegt. INF-Datei kann jedoch später geändert werden. Dynamische Flags können festgelegt und zurücksetzen, indem Sie MAPI-Methoden.
  
Für einen Nachrichtendienst kann in dieser Eigenschaft eine oder mehrere der folgenden Werte festgelegt werden:
  
SERVICE_CREATE_WITH_STORE 
  
> Reserviert. Nicht verwenden.
    
SERVICE_DEFAULT_STORE 
  
> Dynamische. Der Nachrichtendienst enthält des Standard-Informationsspeichers. Eine Benutzeroberfläche zur sollen Bestätigung durch den Benutzer zur Bestätigung vor dem Löschen oder verschieben diesen Dienst das Profil angezeigt werden. 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> Statische. Die Ebene Service-Flag, die festgelegt werden soll, um anzugeben, dass keines der Anbieter in den Dienst zum Angeben eines Identitätswerts verwendet werden kann. Entweder dieses Flag oder SERVICE_PRIMARY_IDENTITY sollte Set, jedoch nicht beide.
    
SERVICE_PRIMARY_IDENTITY 
  
> Geändert werden. Der entsprechende Nachrichtendienst enthält den Anbieter für die primäre Identität für diese Sitzung verwendet. Verwenden Sie [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) , um dieses Flag festzulegen. Entweder dieses Flag oder SERVICE_NO_PRIMARY_IDENTITY sollte Set, jedoch nicht beide. 
    
SERVICE_SINGLE_COPY 
  
> Statische. Jeder Versuch, erstellen oder kopieren Sie diesen Nachrichtendienst in einem Profil, auf dem der Dienst bereits vorhanden ist, schlägt fehl. Zum Erstellen einer einzelnen Kopie Messagingdiensts die **PR_RESOURCE_FLAGS** -Eigenschaft auf den Dienst im Abschnitt MAPISVC hinzufügen. INF-Datei, und legen Sie dieses Flag. 
    
Einem Dienstanbieter kann in **PR_RESOURCE_FLAGS**eines oder mehrere der folgenden Werte festgelegt werden:
  
HOOK_INBOUND 
  
> Statische. Verarbeitung eingehender Nachrichten muss der Warteschlange Hook.
    
HOOK_OUTBOUND 
  
> Statische. Der Warteschlange Hook muss ausgehende Nachrichten verarbeiten. 
    
STATUS_DEFAULT_OUTBOUND 
  
> Geändert werden. Diese Identität werden soll für ausgehende Nachrichten angewendet, wenn das Profil mehrere Instanzen dieser Transportdienst enthält. Dies kann vorkommen, wenn mehrere Instanzen eines einzigen Anbieters im Profil angezeigt werden.
    
STATUS_DEFAULT_STORE 
  
> Geändert werden. Dieses Nachrichtenspeichers ist der Standard-Informationsspeichers für das Profil. 
    
STATUS_NEED_IPM_TREE 
  
> Dynamische. Die standardmäßigen Ordner dieses Nachrichtenspeichers, einschließlich den Stammordner zwischen Personen Nachricht (IPM) wurden nicht überprüft. MAPI festgelegt und löscht dieses Flag. 
    
STATUS_NO_DEFAULT_STORE 
  
> Statische. Dieses Nachrichtenspeichers ist nicht in der Lage sind somit Nachricht Standardspeicher für das Profil.
    
STATUS_NO_PRIMARY_IDENTITY 
  
> Statische. Diesem Anbieter ist nicht mit eine Identität in der Statuszeile sind. Entweder dieses Flag oder STATUS_PRIMARY_IDENTITY muss festgelegt werden.
    
STATUS_OWN_STORE 
  
> Statische. Dieser Transportdienst ist eng mit einem Nachrichtenspeicher verknüpft und stellt die **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md))-Eigenschaft in der Statuszeile bereit.
    
STATUS_PRIMARY_IDENTITY 
  
> Geändert werden. Dieser Anbieter stellt die primäre Identität für die Sitzung bereit; die Eintrags-ID für die Einrichtung der Identity-Objekt wird von [IMAPISession::QueryIdentity](imapisession-queryidentity.md)zurückgegeben. Entweder dieses Flag oder **STATUS_NO_PRIMARY_IDENTITY** muss festgelegt werden. 
    
STATUS_PRIMARY_STORE 
  
> Geändert werden. Dieses Nachrichtenspeichers ist verwendet werden, wenn eine Clientanwendung anmeldet. Nach dem Öffnen, sollte diesen Informationsspeicher als Standardspeicher für das Profil festgelegt werden. 
    
STATUS_SECONDARY_STORE 
  
> Geändert werden. Dieses Nachrichtenspeichers ist geeignet, wenn der primäre Speicher nicht verfügbar ist, wenn eine Clientanwendung anmeldet. Nach dem Öffnen, sollte diesen Informationsspeicher als Standardspeicher für das Profil festgelegt werden. 
    
STATUS_SIMPLE_STORE 
  
> Dynamische. Dieses Nachrichtenspeichers wird als den Standard-Nachrichtenspeicher von Simple MAPI verwendet werden.
    
STATUS_TEMP_SECTION 
  
> Dynamische. Dieses Nachrichtenspeichers sollte nicht in der Nachricht Store Tabelle veröffentlicht werden und wird aus dem Profil nach der Abmeldung gelöscht werden. 
    
STATUS_XP_PREFER_LAST 
  
> Statische. Dieser Transport erwartet in der letzten Übertragungsprotokoll zum Senden einer Nachricht, wenn mehrere Transportanbieter zum Übertragen der Nachricht können ausgewählt werden.
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[PidTagIdentityEntryId (kanonische Eigenschaft)](pidtagidentityentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

