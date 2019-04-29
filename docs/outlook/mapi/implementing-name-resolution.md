---
title: Implementieren der Namensauflösung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4c71b08-c47a-4421-8603-d5356d32dca9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 15c1d502947865c02973f4950b6b6fa8109b8e78
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434704"
---
# <a name="implementing-name-resolution"></a>Implementieren der Namensauflösung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Adressbuchanbieter sind für die Unterstützung der Namensauflösung verantwortlich – der Prozess der Zuordnung eines Eintrags Bezeichners zu einem Anzeigenamen. Clients initiieren die Namensauflösung, wenn Sie [IAddrBook::](iaddrbook-resolvename.md) ResolveName aufrufen, um sicherzustellen, dass jedes Mitglied der Empfängerliste einer ausgehenden Nachricht einer gültigen Adresse entspricht. 
  
Ihr Anbieter kann die Namensauflösung nach folgenden Themen unterstützen:
  
- Unterstützung der **PR_ANR** ([pidtaganr (](pidtaganr-canonical-property.md))-Eigenschaftseinschränkung, eine Anforderung für alle Adressbuchcontainer.
    
- Implementieren der [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) -Methode, eine Option für alle Adressbuchcontainer. 
    
Wenn Sie **IABContainer:: ResolveNames**unterstützen, versuchen Sie, eine exakte Übereinstimmung für jeden nicht aufgelösten Anzeigenamen in der [ADRLIST](adrlist.md) -Struktur zu finden, die mit dem _lpAdrList_ -Parameter übergeben wurde. Sie können einen nicht aufgelösten Anzeigenamen identifizieren, da die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft im Eigenschaftswert Array im **aEntries** -Element der **ADRLIST** -Struktur fehlt. Ignorieren Sie alle Einträge, denen keine Eigenschaften zugeordnet sind. 
  
Melden Sie das Ergebnis des Lösungsversuchs im _lpFlagList_ -Parameter, ein Array von Flags, das dem Array von Anzeigenamen in _lpAdrList_entspricht. Die Flags sind so positioniert, dass das erste Flag dem ersten **aEntries** -Element in der **ADRLIST** -Struktur entspricht, das zweite Flag dem zweiten **aEntries** -Element usw. 
  
Für jeden nicht aufgelösten Eintrag gibt es drei mögliche Ergebnisse:
  
- Es wurde keine Übereinstimmung gefunden, was bedeutet, dass keiner der Einträge in ihren Container Einträgen mit dem Eintrag in der **ADRLIST** -Struktur übereinstimmt. Legen Sie den entsprechenden Eintrag im Parameter _lpFlagList_ auf MAPI_UNRESOLVED. 
    
- Es können mehrere Übereinstimmungen gefunden werden, was bedeutet, dass es mehrere Container Einträge gibt, die mit dem Eintrag in der **ADRLIST** -Struktur übereinstimmen. Legen Sie den entsprechenden Eintrag im Parameter _lpFlagList_ auf MAPI_AMBIGUOUS. Ändern Sie nicht die Anzahl der Einträge in der **ADRLIST** -Struktur. 
    
- Eine exakte Übereinstimmung kann gefunden werden, was bedeutet, dass es nur einen Container Eintrag gibt, der mit dem Eintrag in der **ADRLIST** -Struktur übereinstimmt. Legen Sie den entsprechenden Member im _lpFlagList_ -Parameter auf MAPI_RESOLVED fest, und fügen Sie dem Array von Eigenschaften, das dem **ADRLIST** -Eintrag zugeordnet ist, die Eintrags-ID hinzu. 
    
Wenn Sie **IABContainer:: ResolveNames**nicht unterstützen möchten, geben Sie MAPI_E_NO_SUPPORT aus der Implementierung zurück.
  
Alle Adressbuchanbieter sind zur Unterstützung der mehrdeutigen Namensauflösung – der **PR_ANR** -Eigenschaftseinschränkung – in den Inhaltstabellen der Container erforderlich. Um diese Unterstützung bereitzustellen, behandeln Sie die PR_ANR-Einschränkung in ihrer Implementierung von [IMAPITable:: Restrict](imapitable-restrict.md) , indem Sie einen "bestmöglichen" Suchtyp ausführen, der mit einer oder mehreren bestimmten Eigenschaften übereinstimmt, die für Ihren Anbieter sinnvoll sind. Sie können jederzeit dieselbe Eigenschaft oder Eigenschaften wie **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) oder **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) verwenden oder einem Administrator die Auswahl aus einer Liste akzeptabler Eigenschaften ermöglichen. 
  
Obwohl die meisten Anbieter ihre eigene Inhaltstabellen Implementierung bereitstellen, können Sie die von MAPI bereitgestellte Implementierung [](createtable.md) über die CreateTable-Funktion anpassen. Da die MAPI-Implementierung jedoch keine Einschränkungen unterstützt, müssen Sie ein Wrapperobjekt erstellen, um eine angepasste Version von **Restrict** einzuschließen, die den Anruf abfängt. 
  

