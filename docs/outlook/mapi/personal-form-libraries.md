---
title: Persönliche Formularbibliotheken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1d49cb5c464c27fd121a680d95c588bc7916f232
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571346"
---
# <a name="personal-form-libraries"></a>Persönliche Formularbibliotheken

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wie der Name schon sagt, enthalten persönliche Formularbibliotheken Formulare, die für einen bestimmten Benutzer von Interesse sind. Die persönliche Formularbibliothek eines Benutzers ist die Formularbibliothek, die dem standardnachrichtenspeicher zugeordnet ist, der im Profil des Benutzers angegeben ist. Jedes auf einer Arbeitsstation installierte Profil kann einen separaten Standardspeicher und somit eine separate persönliche Formularbibliothek verwenden. Eine persönliche Formularbibliothek kann Kopien von Formularen enthalten, die zusätzlich zu anderen Formularen auch in anderen Formularbibliotheken enthalten sind.
  
Eine persönliche Formularbibliothek wird im Zugeordneten Inhaltsverzeichnis des Stammordners im Standardnachrichtenspeicher eines Benutzers implementiert – unabhängig davon, ob sich diese auf einem Server oder lokal auf der Arbeitsstation des Benutzers befinden, ist unwesentlich. Wenn der Standardnachrichtenspeicher des Benutzers auf der Arbeitsstation des Benutzers gespeichert ist, bieten persönliche Formularbibliotheken eine verbesserte Leistung, da Anwendungen auf Formulare lokal statt über das Netzwerk zugreifen können. Außerdem werden Formulare für Benutzer verfügbar, die offline arbeiten. Dies kann passieren, wenn Benutzer ihre Formulare auf tragbaren Computern mit ihnen aufnehmen möchten und keinen Zugriff auf ein Netzwerk haben.
  
Die Eigenschaften und die zugrunde liegende Implementierung persönlicher Formularbibliothekseinträge umfassen eine "Container-ID"-Eigenschaft, die einen Mastercontainer identifiziert, mit dem der lokale Eintrag synchronisiert werden muss. Dies kann der Bezeichner eines beliebigen Ordners sein, der Formulare enthält. Dies ist nützlich, wenn Sie einen benutzerdefinierten Formular-Manager verwenden, der eine Art organisationsweite Formularbibliothek unterstützt. Der Formular-Manager kümmert sich um die Synchronisierung der in der persönlichen Formularbibliothek und der organisationsweiten Formularbibliothek gespeicherten Formulare. Dies würde wahrscheinlich passieren, wenn der Formular-Manager geladen wurde, aber theoretisch jederzeit geschehen.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

