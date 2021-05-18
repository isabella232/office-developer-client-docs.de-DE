---
title: Auflösen eines Empfängernamens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a3faed3dda2461cab749c824fc97c2074e62375f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405865"
---
# <a name="resolving-a-recipient-name"></a>Auflösen eines Empfängernamens

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn eine Nachricht adressiert wird, wird eine Empfängerliste mit Eigenschaften erstellt, die sich auf jeden Empfänger bezogen haben. Wenn die Nachricht gesendet wird, muss eine dieser Eigenschaften der langfristige Eintragsbezeichner des Empfängers sein. Um sicherzustellen, dass jeder Empfänger die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft enthält, übergeben Sie die [ADRLIST-Struktur,](adrlist.md) die Ihre Empfängerliste beschreibt, im Inhalt des  _lpAdrList-Parameters_ in einem Aufruf von [IAddrBook::ResolveName](iaddrbook-resolvename.md).
  
 **ResolveName** beginnt mit der Verarbeitung, indem die Einträge in der **ADRLIST-Struktur** ignoriert werden, die bereits aufgelöst wurden, wie durch das Vorhandensein eines Eintragsbezeichners im **SPropValue-Array** der entsprechenden [ADRENTRY-Struktur](adrentry.md) angegeben. Als Nächstes **weist ResolveName** zwei Empfängertypen automatisch einmal zugewiesene Eintragsbezeichner zu: 
  
- Empfänger mit einer als Internetadresse formatierten Adresse
    
- Empfänger mit einer wie folgt formatierten Adresse:
    
     `displayname[address type:email address]`
    
Für alle verbleibenden Einträge durchsucht **ResolveName** das Adressbuch nach einer genauen Übereinstimmung mit dem Anzeigenamen. **ResolveName** verwendet die **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) -Eigenschaft, um den Satz von Zu durchsuchenden Containern und die Suchreihenfolge zu bestimmen. MAPI ruft die [IABContainer::ResolveNames-Methode](iabcontainer-resolvenames.md) jedes Containers auf, um zu versuchen, alle Namen zu auflösen. Da einige Container **ResolveNames** nicht unterstützen, wendet MAPI eine **PR_ANR** - Eigenschaftseinschränkung ([PidTagAnr](pidtaganr-canonical-property.md)) auf die Inhaltstabelle an, wenn der Container MAPI_E_NO_SUPPORT zurückgibt. Alle Adressbuchcontainer sind erforderlich, um die Namensauflösung mit dieser Einschränkung zu unterstützen. Sobald alle Namen aufgelöst wurden, werden keine weiteren Containeraufrufe mehr vorgenommen. Wenn alle Container aufgerufen wurden, aber mehrdeutige oder nicht aufgelöste Namen erhalten bleiben, zeigt MAPI nach Möglichkeit ein Dialogfeld an, in dem der Benutzer aufgefordert wird, die verbleibenden Namen zu auflösen.
  
Die **PR_ANR** entspricht dem Wert der **PR_ANR-Eigenschaft** mit dem Anzeigenamen in der **ADRLIST-Struktur.** Wenn Sie die Ansicht der Inhaltstabelle eines Containers mit der Einschränkung der **PR_ANR-Eigenschaft** einschränken, führt der Adressbuchanbieter eine Suchart "best guess" durch, die mit der für den Anbieter sinnvollen Eigenschaft abgleicht. Beispielsweise kann ein Adressbuchanbieter namen in der Empfängerliste immer mit **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) übereinstimmen, während ein anderer Administrator die Eigenschaft auswählen kann.
  
 **So legen Sie PR_ANR eigenschafteneinschränkung für die Inhaltstabelle eines Adressbuchcontainers**
  
1. Erstellen Sie [eine SRestriction-Struktur,](srestriction.md) wie im folgenden Code dargestellt: 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Rufen Sie die [IMAPITable::Restrict-Methode](imapitable-restrict.md) der Inhaltstabelle auf, und übergeben Sie die **SRestriction-Struktur** als _lpRestriction-Parameter._ 
    

