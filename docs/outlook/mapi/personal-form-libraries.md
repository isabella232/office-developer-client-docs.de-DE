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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348447"
---
# <a name="personal-form-libraries"></a>Persönliche Formularbibliotheken

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wie der Name schon sagt, enthalten persönliche Formularbibliotheken interessante Formulare für einen bestimmten Benutzer. Die persönliche Formularbibliothek eines Benutzers ist die Formularbibliothek, die dem im Profil des Benutzers angegebenen Standardnachrichtenspeicher zugeordnet ist. jedes auf einer Arbeitsstation installierte Profil kann einen separaten Standardspeicher und daher eine separate persönliche Formularbibliothek verwenden. Eine persönliche Formularbibliothek kann Kopien von Formularen enthalten, die zusätzlich zu anderen Formularen auch in anderen Formularbibliotheken enthalten sind.
  
Eine persönliche Formularbibliothek wird in der Tabelle mit den verknüpften Inhalten des Stammordners im Standardnachrichtenspeicher eines Benutzers implementiert, unabhängig davon, ob Sie sich auf einem Server oder lokal auf der Arbeitsstation des Benutzers befindet. Wenn der standardmäßige Nachrichtenspeicher des Benutzers auf der Arbeitsstation des Benutzers gespeichert ist, bieten persönliche Formularbibliotheken eine verbesserte Leistung, da Anwendungen den Zugriff auf Formulare statt über das Netzwerk ermöglichen. Es stellt auch Formulare für Offline arbeitende Benutzer bereit, die auftreten können, wenn Benutzer ihre Formulare auf tragbaren Computern mit sich führen und keinen Zugriff auf ein Netzwerk haben.
  
Zu den Eigenschaften und der zugrunde liegenden Implementierung persönlicher Formular Bibliothekseinträge gehört eine "Container-ID"-Eigenschaft, die einen Master Container identifiziert, mit dem der lokale Eintrag synchronisiert werden muss. Dabei kann es sich um den Bezeichner eines willkürlichen Ordners handeln, der Formulare enthält. Dies ist hilfreich, wenn Sie einen benutzerdefinierten Formular-Manager verwenden, der eine Art organisationsweite Formularbibliothek unterstützt. der Formular Manager würde die in der persönlichen Formularbibliothek gespeicherten Formulare und die organisationsweite Formularbibliothek synchronisieren. Dies würde wahrscheinlich passieren, wenn der Formular-Manager geladen wurde, aber theoretisch jederzeit möglich ist.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

