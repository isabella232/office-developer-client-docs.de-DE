---
title: Persönliche Formularbibliotheken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c84665077f9c8e02647a4d348042515366b0c090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420409"
---
# <a name="personal-form-libraries"></a>Persönliche Formularbibliotheken

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wie der Name schon sagt, enthalten persönliche Formularbibliotheken Formen, die für einen bestimmten Benutzer von Interesse sind. Die persönliche Formularbibliothek eines Benutzers ist die Formularbibliothek, die dem im Benutzerprofil identifizierten Standardnachrichtenspeicher zugeordnet ist. Jedes auf einer Arbeitsstation installierte Profil kann einen separaten Standardspeicher und somit eine separate persönliche Formularbibliothek verwenden. Eine persönliche Formularbibliothek kann Kopien von Formularen enthalten, die zusätzlich zu anderen Formularen auch in anderen Formularbibliotheken enthalten sind.
  
Eine persönliche Formularbibliothek wird im Inhaltsverzeichnis des Stammordners im Standardnachrichtenspeicher eines Benutzers implementiert – unabhängig davon, ob diese sich auf einem Server oder lokal auf der Arbeitsstation des Benutzers befindet, ist unerheblich. Wenn der Standardnachrichtenspeicher des Benutzers auf der Arbeitsstation des Benutzers gespeichert ist, bieten persönliche Formularbibliotheken eine verbesserte Leistung, indem Anwendungen den lokalen Zugriff auf Formulare statt über das Netzwerk ermöglichen. Darüber hinaus stehen Benutzern, die offline arbeiten, Formulare zur Verfügung, die auftreten können, wenn Benutzer ihre Formulare auf tragbaren Computern mit sich nehmen möchten und keinen Zugriff auf ein Netzwerk haben.
  
Die Eigenschaften und die zugrunde liegende Implementierung persönlicher Formularbibliothekseinträge enthalten eine "Container-ID"-Eigenschaft, die einen Mastercontainer identifiziert, mit dem der lokale Eintrag synchronisiert werden muss. Dies kann der Bezeichner eines beliebigen Ordners sein, der Formulare enthält. Dies ist hilfreich, wenn Sie einen benutzerdefinierten Formular-Manager verwenden, der eine Art organisationsweite Formularbibliothek unterstützt. Der Formularmanager kümmert sich um die Synchronisierung der in der persönlichen Formularbibliothek und der organisationsweiten Formularbibliothek gespeicherten Formulare. Dies würde wahrscheinlich passieren, wenn der Formular-Manager geladen wurde, aber theoretisch jederzeit geschehen.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

