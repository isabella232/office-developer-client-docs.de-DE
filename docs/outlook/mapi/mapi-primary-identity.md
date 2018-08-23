---
title: Primäre MAPI-Identität
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: de1fe8fd5ef5a6e79934478c62b2403c48f85b5e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565879"
---
# <a name="mapi-primary-identity"></a>Primäre MAPI-Identität

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die meisten MAPI-Sitzungen vorhanden sind, einen bestimmten Dienstanbieter, der die primäre Identität für die Sitzung bereitstellt. In der Regel ist es Adressbuch-Dienstanbieter, die Identität über Verteilerlisten oder messaging User-Objekte bereitstellt. Tatsächlich empfiehlt MAPI Message-Dienste, die ein Adressbuchanbieter einschließen eines seiner Objekte für die primäre Identität verwenden. Bei ein Dienstanbieter, der eine Message Service gehört die primäre Identität bereitstellt, teilen sich alle anderen-Dienstanbieter in den Dienst diese Identität.
  
Die Datei MAPISVC. INF-Konfigurationsdatei hat Einträge zu Identität am Dienst Message und Service Provider-Ebene. Nachricht Service Abschnitte müssen einen Eintrag enthalten, der angibt, ob der Dienst die primäre Identität angeben kann. Service Provider Abschnitte enthalten einen solchen Eintrag nur, wenn der Anbieter eine Identität angeben kann.
  
Die folgende Tabelle enthält die Einträge, die in den Messagingdiensts und Service Provider Abschnitte in die Datei MAPISVC angezeigt werden. INF-Datei.
  
|**Primäre Identität Lieferanten**|**PR_RESOURCE_FLAGS-Einstellung**|
|:-----|:-----|
|Messagingdiensts  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|Nicht den Dienst  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|Dienstanbieter  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
Mehrere Nachrichtendienste für die können Sie ihre Fähigkeit zum Bereitstellen einer Sitzung primäre Identität deklarieren, wird nur eine Messagingdiensts dazu ausgewählt. Auswahl dieser Option kann auftreten:
  
- Wenn ein Profil erstellt wird.
    
- Wenn ein Client **IMsgServiceAdmin::SetPrimaryIdentity** explizit einen bestimmte Nachricht-Dienst als Anbieter der Sitzung Identität herstellen aufruft. Weitere Informationen. Finden Sie unter [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).
    
Wenn ein Profil erstellt wird, legt MAPI den ersten Nachrichtendienst konfiguriert werden soll, der mit dem STATUS_PRIMARY_IDENTITY-Flag, legen Sie in dessen **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))-Eigenschaft auf die primäre Identität angeben ein Anbieters enthält fest. . Innerhalb der festgelegten Messagingdiensts wird der erste Anbieter mit dieser Kennzeichnung Ressourcensatz konfiguriert werden ausgewählt, um die Identität für den Dienst bereitzustellen. Das Flag STATUS_PRIMARY_IDENTITY ist für alle anderen Anbieter in den festgelegten Dienst und andere Nachrichtendienste im Profil gelöscht. Wenn können Sie jederzeit der Anbieter angeben primären Identität aus dem Profil entfernt wird, weist MAPI die Rolle an den nächsten Anbieter konfiguriert werden soll, die Identität angeben kann. Dies wird durch die Darstellung des bestimmt die `PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY` Eintrag im Abschnitt MAPISVC.INF des Anbieters. 
  
Wenn ein Client eine Messagingdiensts **IMsgServiceAdmin::SetPrimaryIdentity** -Methode aufruft, gibt die MAPIUID für einen Dienstanbieter innerhalb der Zieldienst an. Weitere Informationen finden Sie unter [MAPIUID](mapiuid.md). Der Dienstanbieter, dargestellt durch die **MAPIUID** zugeordnet ist, geben Sie die primäre Identität für den Dienst und für die Sitzung, und alle anderen Anbieter im Dienst wird diese Identität freigeben. 
  
Jeder Anbieter in den Dienst verantwortlich für die Angabe der primären Identität aktualisiert eine Zeile in der Statustabelle "auf die folgenden Eigenschaften enthalten.
  
|**Primäre Identity-Eigenschaft**|**Festgelegt auf**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))  <br/> |Der Anzeigename des-Objekts die primäre Identität angeben.  <br/> |
|**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))  <br/> |Search-Schlüssel für das Objekt, das die primäre Identität angeben.  <br/> |
|**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))  <br/> |Entry-ID für das Objekt, das die primäre Identität angeben.  <br/> |
   
 **Zum Abrufen der Eintrags-ID für das Objekt, das die primäre Identität angeben**
  
- Rufen Sie die **IMAPISession::QueryIdentity** -Methode. Weitere Informationen finden Sie unter [IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** sucht in der Statustabelle "für die Zeile, die den Wert STATUS_PRIMARY_IDENTITY in die Spalte **PR_RESOURCE_FLAGS** enthält, und gibt die entsprechenden **PR_IDENTITY_ENTRYID** als die Eintrags-ID für die primäre Identität. 
    

