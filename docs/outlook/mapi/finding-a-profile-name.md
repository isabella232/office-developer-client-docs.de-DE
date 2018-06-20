---
title: Suchen einen Profilnamen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 332b78bcebbcd54de43376553ec4aea386c1c359
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791682"
---
# <a name="finding-a-profile-name"></a>Suchen einen Profilnamen

  
  
**Betrifft**: Outlook 
  
In einigen Fällen müssen Clients suchen den Namen des Profils wird derzeit für die Sitzung, den Namen des Standardprofils oder den Namen eines alternativen Profils auf dem Computer installierten verwendet.
  
Es gibt einige Methoden zum Abrufen des Namens eines Profils im Laufe einer Sitzung. Wenn Sie den Namen eines Profils zu suchen, die nicht unbedingt für die Sitzung verwendet werden müssen, verwenden Sie das erste Verfahren. Wenn Sie den Namen des Standardprofils suchen müssen, verwenden Sie das zweite Verfahren. Wenn Sie den Namen des aktuellen Profils für die Sitzung zu suchen möchten, verwenden Sie das letzte Verfahren. 
  
 **Suchen Sie den Namen Profil**
  
1. Rufen Sie ["MAPIAdminProfiles"](mapiadminprofiles.md) zum Abrufen eines **IProfAdmin** Schnittstelle Zeigers. 
    
2. Rufen Sie [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) Zugriff auf die Benutzerprofildienst-Tabelle. 
    
3. Rufen Sie [die Profiltabelle QueryRows zum Abrufen aller Zeilen in der Tabelle und Untersuchen von jedem Befehl die EINGABETASTE, um zu bestimmen, ob sie Ihr Zielprofil darstellt](imapitable-queryrows.md) . 
    
 **Der Name des Standardprofils gefunden**
  
1. Rufen Sie ["MAPIAdminProfiles"](mapiadminprofiles.md).
    
2. Rufen Sie [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) Zugriff auf die Benutzerprofildienst-Tabelle. 
    
3. Erstellen Sie eine eigenschaftseinschränkung mit einer [SPropertyRestriction](spropertyrestriction.md) Struktur, der **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) mit dem Wert TRUE entspricht.
    
4. Rufen Sie [IMAPITable](imapitable-findrow.md) , um die Zeile in der Profiltabelle zu suchen, die das Standardprofil darstellt. Die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Spalte enthält den Namen des Standardprofils.
    
 **Der Name des aktuellen Profils gefunden**
  
Führen Sie die folgenden Schritte aus, um den Namen des aktuellen Profils zu finden:
  
- Unter der Annahme, dass Sie die [MAPIUID](mapiuid.md) -Struktur, die einen der Abschnitte für das aktuelle Profil darstellt haben, übergeben Sie sie an [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)im _LpUID_ -Parameter. Rufen Sie das Profilabschnitt **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md))-Eigenschaft mithilfe der Methode [IMAPIProp::GetProps](imapiprop-getprops.md) ab. 
    
- Rufen Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md) Zugriff auf die Statustabelle, und suchen Sie die Zeile, die die **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))-Spalte auf MAPI_SUBSYSTEM festgelegt wurde. Die **PR_DISPLAY_NAME** Spalte für diese Zeile ist der Name der Benutzerprofildienst. Verwenden Sie nicht die Statustabelle während des Starts von, da es eine Anwendung blockiert, bis die MAPI-Warteschlange die Initialisierung aller Transportanbieter für den abgeschlossen hat. Dies kann die Leistung beeinträchtigen. 
    

