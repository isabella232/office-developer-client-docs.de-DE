---
title: Primäre MAPI-Identität
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dd0ffa1d8c9d2b8b8a65fd8434fc382f6ee77547
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610237"
---
# <a name="mapi-primary-identity"></a>Primäre MAPI-Identität

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die meisten MAPI-Sitzungen verfügen über einen bestimmten Dienstanbieter, der die primäre Identität für die Sitzung bereitstellt. In der Regel handelt es sich um einen Adressbuchanbieter, der Identität über eines seiner Messagingbenutzerobjekte oder Verteilerlisten bereitstellt. Tatsächlich empfiehlt mapi, dass Nachrichtendienste, die einen Adressbuchanbieter enthalten, eines seiner Objekte für die primäre Identität verwenden. Wenn ein Dienstanbieter, der zu einem Nachrichtendienst gehört, die primäre Identität bereitstellt, teilen sich alle anderen Dienstanbieter im Nachrichtendienst diese Identität.
  
The MAPISVC. Die INF-Konfigurationsdatei enthält Einträge, die sich auf die Identität auf Nachrichtendienst- und Dienstanbieterebene beziehen. Nachrichtendienstabschnitte müssen einen Eintrag enthalten, der angibt, ob der Dienst die primäre Identität bereitstellen kann. Dienstanbieterabschnitte enthalten einen ähnlichen Eintrag nur, wenn der Anbieter eine Identität angeben kann.
  
In der folgenden Tabelle sind die Einträge aufgeführt, die in den Abschnitten "Nachrichtendienst" und "Dienstanbieter" in MAPISVC angezeigt werden. INF-Datei.
  
|**Primärer Identitätsanbieter**|**einstellung für PR_RESOURCE_FLAGS**|
|:-----|:-----|
|Nachrichtendienst  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|Nicht der Nachrichtendienst  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|Dienstleister  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
Obwohl mehrere Nachrichtendienste ihre Fähigkeit deklarieren können, die primäre Identität einer Sitzung bereitzustellen, wird dafür nur ein Nachrichtendienst ausgewählt. Diese Auswahl kann auftreten:
  
- Wenn ein Profil erstellt wird.
    
- Wenn ein Client **IMsgServiceAdmin::SetPrimaryIdentity aufruft,** um explizit einen bestimmten Nachrichtendienst als Anbieter der Sitzungsidentität einzurichten. Weitere Informationen. Siehe [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).
    
Wenn ein Profil erstellt wird, bestimmt DIE MAPI den ersten Zu konfigurierenden Nachrichtendienst, der einen Anbieter mit dem in der **eigenschaft PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festgelegten STATUS_PRIMARY_IDENTITY-Flag enthält, um die primäre Identität zu liefern. Innerhalb des angegebenen Nachrichtendiensts wird der erste Anbieter ausgewählt, der mit diesem Ressourcenflag konfiguriert wird, um die Identität für den Dienst bereitzustellen. Das flag STATUS_PRIMARY_IDENTITY wird für alle anderen Anbieter im angegebenen Dienst und andere Nachrichtendienste im Profil deaktiviert. Wenn der Anbieter, der die primäre Identität bereitstellt, zu einem beliebigen Zeitpunkt aus dem Profil entfernt wird, weist mapi die Rolle dem nächsten Anbieter zu, der konfiguriert werden soll, der Identität bereitstellen kann. Dies wird durch die Darstellung des  `PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY` Eintrags im Abschnitt des Anbieters in MAPISVC.INF bestimmt. 
  
Wenn ein Client die **IMsgServiceAdmin::SetPrimaryIdentity-Methode** eines Nachrichtendiensts aufruft, gibt er die MAPIUID für einen Dienstanbieter innerhalb des Zieldiensts an. Weitere Informationen finden Sie unter [MAPIUID](mapiuid.md). Der Dienstanbieter, der durch **die MAPIUID** dargestellt wird, wird zugewiesen, um die primäre Identität für den Nachrichtendienst und für die Sitzung zu liefern, und alle anderen Anbieter im Dienst teilen diese Identität. 
  
Jeder Anbieter im Nachrichtendienst, der für die Bereitstellung der primären Identität verantwortlich ist, aktualisiert seine Zeile in der Statustabelle, um die folgenden Eigenschaften einzuschließen.
  
|**Primäre Identitätseigenschaft**|**Festgelegt auf**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))  <br/> |Anzeigename des Objekts, das die primäre Identität angibt.  <br/> |
|**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))  <br/> |Suchschlüssel für das Objekt, das die primäre Identität angibt.  <br/> |
|**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))  <br/> |Eintragsbezeichner für das Objekt, das die primäre Identität angibt.  <br/> |
   
 **So rufen Sie den Eintragsbezeichner für das Objekt ab, das die primäre Identität angibt**
  
- Rufen Sie die **IMAPISession::QueryIdentity-Methode** auf. Weitere Informationen finden Sie unter [IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** durchsucht die Statustabelle nach der Zeile, die den Wert STATUS_PRIMARY_IDENTITY in der **spalte PR_RESOURCE_FLAGS** enthält, und gibt die entsprechende **PR_IDENTITY_ENTRYID** als Eintragsbezeichner für die primäre Identität zurück. 
    

