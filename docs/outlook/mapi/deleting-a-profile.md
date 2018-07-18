---
title: Löschen eines Profils
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 29e7806afce885968956d53005a66bd14639ad64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791515"
---
# <a name="deleting-a-profile"></a>Löschen eines Profils

  
  
**Betrifft**: Outlook 
  
 **Zum Löschen eines Profils**
  
- Rufen Sie [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** markiert das Profil zum Löschen, wenn es derzeit warten verwendet wird, bis es nicht mehr entfernen aktiv ist. Das Profil wird nicht tatsächlich ausgeblendet, bis jeder Client mit einer aktiven Sitzung unterbrochen hat. 
  
 **DeleteProfile** Ruft die Eintrags-Funktion von jeder Nachrichtendienst im Profil mit dem _UlContext_ -Parameter auf MSG_SERVICE_DELETE festgelegt. Die Aufrufe an den Eintrag Punktfunktionen tritt auf, bevor die Dienste physisch aus dem Profil entfernt werden. 
  

