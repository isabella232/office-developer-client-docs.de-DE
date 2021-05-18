---
title: PRIMÄRE MAPI-Identität
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5bf88de280b012c54d4caaac6bdfe877f476ac37
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404722"
---
# <a name="mapi-primary-identity"></a>PRIMÄRE MAPI-Identität

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die meisten MAPI-Sitzungen verfügen über einen bestimmten Dienstanbieter, der die primäre Identität für die Sitzung liefert. In der Regel handelt es sich um einen Adressbuchanbieter, der Identität über eines seiner Messagingbenutzerobjekte oder Verteilerlisten liefert. In der Tat empfiehlt MAPI, dass Nachrichtendienste, die einen Adressbuchanbieter enthalten, eines ihrer Objekte für die primäre Identität verwenden. Wenn ein Dienstanbieter, der zu einem Nachrichtendienst gehört, die primäre Identität liefert, teilen sich alle anderen Dienstanbieter im Nachrichtendienst diese Identität.
  
Der MAPISVC. Die INF-Konfigurationsdatei enthält Einträge zur Identität auf Nachrichtendienst- und Dienstanbieterebene. Die Abschnitte des Nachrichtendiensts müssen einen Eintrag enthalten, der antrat, ob der Dienst die primäre Identität liefern kann. Dienstanbieterabschnitte enthalten einen ähnlichen Eintrag nur, wenn der Anbieter eine Identität liefern kann.
  
In der folgenden Tabelle sind die Einträge aufgeführt, die in den Abschnitten nachrichtendienst und Dienstanbieter in MAPISVC angezeigt werden. INF-Datei.
  
|**Primärer Identitätsanbieter**|**PR_RESOURCE_FLAGS-Einstellung**|
|:-----|:-----|
|Nachrichtendienst  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|Nicht der Nachrichtendienst  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|Dienstanbieter  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
Obwohl mehrere Nachrichtendienste ihre Fähigkeit zum Bereitstellen der primären Identität einer Sitzung deklarieren können, ist dafür nur ein Nachrichtendienst ausgewählt. Diese Auswahl kann auftreten:
  
- Wenn ein Profil erstellt wird.
    
- Wenn ein Client **IMsgServiceAdmin::SetPrimaryIdentity** aufruft, um explizit einen bestimmten Nachrichtendienst als Anbieter der Sitzungsidentität zu erstellen. Weitere Informationen. Weitere Informationen finden Sie [unter IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).
    
Wenn ein Profil erstellt wird, bestimmt MAPI den ersten zu konfigurierenden Nachrichtendienst, der einen Anbieter mit dem STATUS_PRIMARY_IDENTITY-Flag enthält, das in seiner **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))-Eigenschaft festgelegt ist, um die primäre Identität zu liefern. Innerhalb des festgelegten Nachrichtendiensts wird der erste Anbieter ausgewählt, der mit diesem Ressourcenflagsatz konfiguriert werden soll, um die Identität für den Dienst zur Verfügung zu stellen. Das STATUS_PRIMARY_IDENTITY wird für alle anderen Anbieter im angegebenen Dienst und andere Nachrichtendienste im Profil geräumt. Wenn der Anbieter, der die primäre Identität liefert, jederzeit aus dem Profil entfernt wird, weist MAPI die Rolle dem nächsten zu konfigurierenden Anbieter zu, der Identität liefern kann. Dies wird durch die Darstellung des Eintrags im Abschnitt des Anbieters  `PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY` in MAPISVC.INF bestimmt. 
  
Wenn ein Client die **IMsgServiceAdmin::SetPrimaryIdentity-Methode** eines Nachrichtendiensts aufruft, gibt er die MAPIUID für einen Dienstanbieter innerhalb des Zieldiensts an. Weitere Informationen finden Sie unter [MAPIUID](mapiuid.md). Der durch die **MAPIUID** dargestellte Dienstanbieter wird zugewiesen, um die primäre Identität für den Nachrichtendienst und für die Sitzung zu liefern, und alle anderen Anbieter im Dienst teilen diese Identität. 
  
Jeder Anbieter im Nachrichtendienst, der für die Bereitstellung der primären Identität zuständig ist, aktualisiert seine Zeile in der Statustabelle, um die folgenden Eigenschaften zu enthalten.
  
|**Primäre Identitätseigenschaft**|**Festgelegt auf**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))  <br/> |Anzeigename des Objekts, das die primäre Identität liefert.  <br/> |
|**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))  <br/> |Suchtaste für das Objekt, das die primäre Identität liefert.  <br/> |
|**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))  <br/> |Eintrags-ID für das Objekt, das die primäre Identität liefert.  <br/> |
   
 **So rufen Sie die Eintrags-ID für das Objekt ab, das die primäre Identität liefert**
  
- Rufen Sie die **IMAPISession::QueryIdentity-Methode** auf. Weitere Informationen finden Sie unter [IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** durchsucht die Statustabelle nach der Zeile, die den Wert STATUS_PRIMARY_IDENTITY in der spalte **PR_RESOURCE_FLAGS** enthält, und gibt die entsprechende **PR_IDENTITY_ENTRYID** als Eintrags-ID für die primäre Identität zurück. 
    

