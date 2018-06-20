---
title: Erstellen ein Profil mithilfe der Profil-Assistent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 29a135264772847a624e1a4558b68bcf822b18df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791480"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a>Erstellen ein Profil mithilfe der Profil-Assistent

  
  
**Betrifft**: Outlook 
  
Der Profil-Assistent ist ein MAPI-Feature, mit dem einen Benutzer zum Erstellen eines Profils in die einfachste Möglichkeit. Der Profil-Assistent zeigt eine Reihe von Dialogfeldern in dem der Benutzer aufgefordert, wählen Sie Nachrichtendienste, und geben Sie Werte für einige der wichtigsten Konfigurationseigenschaften. Für die meisten anderen erforderlichen Eigenschaften verwendet der Profil-Assistent Standardwerte bereitgestellt. Rufen Sie zum Aufrufen der Profil-Assistent **LaunchWizard**, eine Funktion, die basierend auf den [LAUNCHWIZARDENTRY](launchwizardentry.md) Prototyp. 
  
Der Benutzer kann nur die Message-Dienste und -Dienstanbieter hinzufügen, um das neue Profil, die die Profile-Assistent unterstützt. Da jede Messagingdiensts möglicherweise mehr Eigenschaften benötigt festgelegt werden soll, als der Profil-Assistent verarbeitet werden können, achten Sie darauf, dass, wenn Sie dieses Verfahren verwenden, für eine oder mehrere der ausgewählten Dienste oder Anbieter unvollständig konfiguriert werden kann.
  

