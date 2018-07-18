---
title: Öffnen ein Adressbuchcontainer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Zuletzt geändert: 08 November 2011'
ms.openlocfilehash: 28f60154524065bd2c818e2e4b7db37ca33276b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793313"
---
# <a name="opening-an-address-book-container"></a>Öffnen ein Adressbuchcontainer

**Betrifft**: Outlook 
  
Nach dem Öffnen der MAPI-Adressbuch integriert, öffnen Sie eine oder mehrere Address Book Containern Zugriff auf die darin enthaltenen Empfänger.
  
Rufen Sie zum Öffnen den Container der obersten Ebene des Adressbuchs [IAddrBook::OpenEntry](iaddrbook-openentry.md) mit einem NULL-Eintrags-ID ein. 
  
Address Book Containern können implementiert werden, mit der nur-Lese- oder Lese-/Schreibzugriff. Nur-Lese-Containern dienen nur zum Durchsuchen. Lese-Schreib-Container können geändert werden, dass Clients, die zum Erstellen neuer Einträge und löschen und Ändern der vorhandenen Einträge. Alle Persönliches Adressbuch (PAB) Container werden als Container für Lese-/Schreibzugriff implementiert. 
  
Zum Öffnen ein unteren Ebene Containers rufen Sie **OpenEntry auf** , und geben Sie die Eintrags-ID des Containers geöffnet werden soll. 
  
## <a name="open-the-container-designated-as-the-pab"></a>Öffnen Sie den Container der PAB als
  
1. Rufen Sie [IAddrBook::GetPAB](iaddrbook-getpab.md) , um die PAB-Eintrags-ID abzurufen. 
    
2. Übergeben Sie dieses Eintrags-ID an [IAddrBook::OpenEntry](iaddrbook-openentry.md).
    
## <a name="open-a-container-that-is-not-the-pab"></a>Öffnen Sie einen Container, der nicht die PAB ist
  
1. Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md) mit einen NULL-Eintrags-ID im Adressbuch Stammcontainer öffnen. 
    
2. Rufen Sie den Container Root [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) -Methode zum Abrufen der Hierarchietabelle – eine Liste aller Container der obersten Ebene im Adressbuch. 
    
3. Wenn der Container zum Öffnen eines bestimmten Typs ist:
    
   - Erstellen Sie eine **SPropertyRestriction** -Struktur mit **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) für das Eigenschafts-Tag, das Container-Typ für den Eigenschaftswert und RELOP_EQ für die Beziehung. **PR_DISPLAY_TYPE** können auf viele Werte, zwischen ihnen festgelegt werden: 
    
   - DT_GLOBAL die Hierarchietabelle Containern beschränken, die in der globalen Adressliste gehören.
    
   - DT_LOCAL die Tabelle, die zu einem lokalen Adressbuch gehören Containern beschränken.
    
   - DT_MODIFIABLE die Tabelle Containern beschränken, die geändert werden kann.
    
   - Erstellen einer [SPropTagArray](sproptagarray.md) -Struktur, die **PR_ENTRYID** **PR_DISPLAY_TYPE**und alle anderen Spalten von Interesse enthält. 
    
   - Rufen Sie [HrQueryAllRows](hrqueryallrows.md), Ihre eigenschaftseinschränkung und Tag-Array-Eigenschaft übergeben. NULL oder mehr Zeilen, eine Zeile für jedes Container, in den angegebenen Typ gehört, gibt **HrQueryAllRows** zurück. Bereiten Sie die Rückgabe einer beliebigen Anzahl von Zeilen zu behandeln. 
    
   - Rufen Sie **IAddrBook::OpenEntry** , wobei die Eintrags-ID aus der **PR_ENTRYID** -Spalte der Zeile, die den Container von Interesse darstellt. 
    
4. Zugehörigkeit der Container zum Öffnen einer bestimmten Adressbuchanbieter:
    
   - Erstellen Sie eine [SPropertyRestriction](spropertyrestriction.md) -Struktur mit **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) für das Eigenschafts-Tag, anbieterspezifische Wert für den Eigenschaftswert und RELOP_EQ für die Beziehung. In der Regel ist der Wert der anbieterspezifische einen global eindeutigen Bezeichner oder eine GUID. Sie finden dieses Werts in eine der Headerdateien der Adressbuchanbieter veröffentlicht. 
    
   - Erstellen einer [SPropTagArray](sproptagarray.md) -Struktur, die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**und alle anderen Spalten von Interesse enthält. 
    
   - Rufen Sie [HrQueryAllRows](hrqueryallrows.md), Ihre eigenschaftseinschränkung und Tag-Array-Eigenschaft übergeben. **HrQueryAllRows** gibt 0 (null) Zeilen zurück, wenn die angegebene Adressbuchanbieter nicht im Profil vorhanden ist. Sie können eine oder mehrere Zeilen für den Anbieter Container auf oberster Ebene, je nach der Struktur des Anbieters zurück. 
    
   - Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md) , wobei die Eintrags-ID aus der **PR_ENTRYID** -Spalte der Zeile, die den Container von Interesse darstellt. Ist der Container, dem Sie interessiert sind nicht Container der obersten Ebene, suchen Sie den Container der obersten Ebene, und Durchlaufen der Hierarchie. 
    

