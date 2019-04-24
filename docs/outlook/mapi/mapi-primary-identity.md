---
title: Primäre MAPI-Identität
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5bf88de280b012c54d4caaac6bdfe877f476ac37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345795"
---
# <a name="mapi-primary-identity"></a>Primäre MAPI-Identität

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die meisten MAPI-Sitzungen verfügen über einen bestimmten Dienstanbieter, der die primäre Identität für die Sitzung bereitstellt. In der Regel handelt es sich um einen Adressbuchanbieter, der die Identität über eines seiner Messaging-Benutzerobjekte oder-Verteilerlisten bereitstellt. In der Tat empfiehlt MAPI, dass Nachrichtendienste, die einen Adressbuchanbieter einbeziehen, eines ihrer Objekte für die primäre Identität verwenden. Wenn ein Dienstanbieter, der zu einem Nachrichtendienst gehört, die primäre Identität bereitstellt, teilen alle anderen Dienstanbieter im Nachrichtendienst diese Identität.
  
Die MAPISVC. Die INF-Konfigurationsdatei enthält Einträge, die sich auf die Identität der Nachrichtendienst-und Dienstanbieter Ebene beziehen. Nachrichtendienst Abschnitte müssen einen Eintrag enthalten, der angibt, ob der Dienst die primäre Identität angeben kann. Dienstanbieter Abschnitte enthalten einen ähnlichen Eintrag nur, wenn der Anbieter eine Identität angeben kann.
  
In der folgenden Tabelle sind die Einträge aufgeführt, die in den Abschnitten Nachrichtendienst und Dienstanbieter in der MAPISVC angezeigt werden. INF-Datei.
  
|**Primärer Identitäts Lieferant**|**PR_RESOURCE_FLAGS-Einstellung**|
|:-----|:-----|
|Nachrichtendienst  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|Nicht der Nachrichtendienst  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|Dienstanbieter  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
Obwohl mehrere Nachrichtendienste ihre Fähigkeit zur Bereitstellung der primären Identität einer Sitzung deklarieren können, wird nur ein Nachrichtendienst dafür ausgewählt. Diese Auswahl kann auftreten:
  
- Beim Erstellen eines Profils.
    
- Wenn ein Client **IMsgServiceAdmin:: SetPrimaryIdentity** aufruft, um einen bestimmten Nachrichtendienst explizit als Anbieter der Sitzungs Identität einzurichten. Weitere Informationen. Weitere Informationen finden Sie unter [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).
    
Bei der Erstellung eines Profils bestimmt MAPI den ersten zu konfigurierenden Nachrichtendienst, der einen Anbieter mit dem STATUS_PRIMARY_IDENTITY-Flag enthält, das in seiner **PR_RESOURCE_FLAGS** ([pidtagresourceflags (](pidtagresourceflags-canonical-property.md))-Eigenschaft festgelegt ist, um die primäre Identität bereitzustellen. . Innerhalb des angegebenen Nachrichtendiensts wird der erste Anbieter, der mit diesem Ressourcen-Flagsatz konfiguriert werden soll, ausgewählt, um die Identität für den Dienst anzugeben. Das STATUS_PRIMARY_IDENTITY-Flag wird für alle anderen Anbieter im angegebenen Dienst und andere Nachrichtendienste im Profil deaktiviert. Wenn der Anbieter, der primäre Identität bereitstellt, zu einem beliebigen Zeitpunkt aus dem Profil entfernt wird, weist MAPI die Rolle dem nächsten zu konfigurierenden Anbieter zu, der die Identität angeben kann. Dies wird durch die Darstellung des `PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY` Eintrags im Abschnitt des Anbieters in MAPISVC. inf bestimmt. 
  
Wenn ein Client die **IMsgServiceAdmin:: SetPrimaryIdentity** -Methode eines Nachrichtendiensts aufruft, gibt er die MAPIUID für einen Dienstanbieter innerhalb des Zieldiensts an. Weitere Informationen finden Sie unter [MAPIUID](mapiuid.md). Der Dienstanbieter, der durch das **MAPIUID** dargestellt wird, wird zugewiesen, um die primäre Identität für den Nachrichtendienst und für die Sitzung bereitzustellen, und alle anderen Anbieter im Dienst teilen diese Identität. 
  
Jeder Anbieter im Nachrichtendienst, der für die primäre Identität zuständig ist, aktualisiert seine Zeile in der Statustabelle mit den folgenden Eigenschaften.
  
|**Primäre Identitätseigenschaft**|**Festgelegt auf**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY** ([Pidtagidentitydisplay (](pidtagidentitydisplay-canonical-property.md))  <br/> |Anzeigename des Objekts, das die primäre Identität bereitstellt.  <br/> |
|**PR_IDENTITY_SEARCH_KEY** ([Pidtagidentitysearchkey (](pidtagidentitysearchkey-canonical-property.md))  <br/> |Suchschlüssel für das Objekt, das die primäre Identität bereitstellt.  <br/> |
|**PR_IDENTITY_ENTRYID** ([Pidtagidentityentryid (](pidtagidentityentryid-canonical-property.md))  <br/> |Eintragsbezeichner für das Objekt, das die primäre Identität bereitstellt.  <br/> |
   
 **So rufen Sie die Eintrags-ID für das Objekt ab, das die primäre Identität bereitstellt**
  
- Rufen Sie die **IMAPISession:: QueryIdentity** -Methode auf. Weitere Informationen finden Sie unter [IMAPISession:: QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** durchsucht die Statustabelle nach der Zeile, die den Wert STATUS_PRIMARY_IDENTITY in der **PR_RESOURCE_FLAGS** -Spalte enthält, und gibt die entsprechende **PR_IDENTITY_ENTRYID** als Eintrags-ID für den primären Identität. 
    

