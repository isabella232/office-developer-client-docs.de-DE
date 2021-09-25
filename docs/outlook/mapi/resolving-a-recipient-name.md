---
title: Auflösen eines Empfängernamens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5f0e1572c3d02707cc50d2e3f9f4747339ad93f5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624349"
---
# <a name="resolving-a-recipient-name"></a>Auflösen eines Empfängernamens

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn eine Nachricht adressiert wird, wird eine Empfängerliste mit Eigenschaften erstellt, die sich auf jeden Empfänger beziehen. Bis zum Senden der Nachricht muss eine dieser Eigenschaften der langfristige Eintragsbezeichner des Empfängers sein. Um sicherzustellen, dass jeder Empfänger die **Eigenschaft PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) enthält, übergeben Sie die [ADRLIST-Struktur,](adrlist.md) die Ihre Empfängerliste im Inhalt des  _lpAdrList-Parameters_ in einem Aufruf von [IAddrBook::ResolveName](iaddrbook-resolvename.md)beschreibt.
  
 **ResolveName** beginnt mit der Verarbeitung, indem die Einträge in der **ADRLIST-Struktur** ignoriert werden, die bereits aufgelöst wurden, wie durch das Vorhandensein eines Eintragsbezeichners im **SPropValue-Array** der entsprechenden [ADRENTRY-Struktur](adrentry.md) angegeben. Als Nächstes weist **ResolveName** zwei Empfängertypen automatisch einmalige Eintragsbezeichner zu: 
  
- Empfänger mit einer als Internetadresse formatierten Adresse
    
- Empfänger mit einer wie folgt formatierten Adresse:
    
     `displayname[address type:email address]`
    
Für alle verbleibenden Einträge durchsucht **ResolveName** das Adressbuch nach einer genauen Übereinstimmung mit dem Anzeigenamen. **ResolveName** verwendet die **eigenschaft PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), um die Gruppe der zu durchsuchenden Container und die Suchreihenfolge zu bestimmen. MAPI ruft die [IABContainer::ResolveNames-Methode](iabcontainer-resolvenames.md) jedes Containers auf, um zu versuchen, alle Namen aufzulösen. Da einige Container **ResolveNames** nicht unterstützen, wendet MAPI, wenn der Container MAPI_E_NO_SUPPORT zurückgibt, eine PR_ANR eigenschaftseinschränkung ([PidTagAnr](pidtaganr-canonical-property.md)) auf das Inhaltsverzeichnis an.  Alle Adressbuchcontainer sind erforderlich, um die Namensauflösung mit dieser Einschränkung zu unterstützen. Nachdem alle Namen aufgelöst wurden, werden keine weiteren Containeraufrufe ausgeführt. Wenn alle Container aufgerufen wurden, aber mehrdeutige oder nicht aufgelöste Namen verbleiben, zeigt MAPI nach Möglichkeit ein Dialogfeld an, in dem der Benutzer aufgefordert wird, die verbleibenden Namen aufzulösen.
  
Die **PR_ANR** Einschränkung entspricht dem Wert der **PR_ANR-Eigenschaft** mit dem Anzeigenamen in der **ADRLIST-Struktur.** Das Einschränken der Ansicht eines Containerinhaltsverzeichnisses mit der **PR_ANR** Eigenschaftseinschränkung bewirkt, dass der Adressbuchanbieter eine Suche vom Typ "am besten erraten" durchführt, die mit der eigenschaft übereinstimmt, die für den Anbieter sinnvoll ist. Beispielsweise kann ein Adressbuchanbieter namen in der Empfängerliste immer mit **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) übereinstimmen, während ein anderer ein Administrator die Eigenschaft auswählen kann.
  
 **So legen Sie eine PR_ANR Eigenschaftseinschränkung für das Inhaltsverzeichnis eines Adressbuchcontainers fest**
  
1. Erstellen Sie eine [SRestriction-Struktur,](srestriction.md) wie im folgenden Code dargestellt: 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. Rufen Sie die [IMAPITable::Restrict-Methode](imapitable-restrict.md) des Inhaltsverzeichnisses auf, und übergeben Sie die **SRestriction-Struktur** als _lpRestriction-Parameter._ 
    

