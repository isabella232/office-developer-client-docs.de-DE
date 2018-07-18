---
title: Eigene Formularbibliotheken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ffcd93c-3737-4342-9cd0-2ca7c0fba52c
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0793fefd744eecc95899c4166cb8a1a6a2e6cd2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793343"
---
# <a name="personal-form-libraries"></a>Eigene Formularbibliotheken

  
  
**Betrifft**: Outlook 
  
Wie der Name schon sagt, enthalten persönliche Formularbibliotheken Formulare für einen bestimmten Benutzer von Interesse an. Ein Benutzer Persönliche Formularbibliothek ist der Formularbibliothek, die im Profil des Benutzers identifizierten Standard-Informationsspeicher zugeordnet. jedes Profil auf einer Arbeitsstation installiert können eine separate Standardspeicher und daher eine separate persönliche Formularbibliothek. Eine persönliche Formularbibliothek kann Kopien Formulare enthalten, die auch in anderen Formularbibliotheken zusätzlich zu anderen Formen enthalten sind.
  
In der Tabelle verknüpfte Inhalt des Stammordners in Nachricht-Standardspeicher des Benutzers ist eine persönliche Formularbibliothek implementiert – ob, die auf einem Server oder lokal auf dem Computer des Benutzers befindet, ist unerheblich. Wenn Message-Standardspeicher des Benutzers auf dem Computer des Benutzers gespeichert ist, bieten persönliche Formularbibliotheken verbesserte Leistung durch Aktivieren von Clientanwendungen auf Formulare lokal anstelle von über das Netzwerk zugreifen. Es wird auch angezeigt Formulare Offlinearbeit, Benutzern die kann auftreten, wenn Benutzer ihre Formulare auf tragbaren Computern mit ihnen zu übernehmen möchten und ohne Zugriff auf ein Netzwerk sind.
  
Die Eigenschaften und die zugrunde liegende Implementierung der persönlichen Formular Bibliothek Einträge enthalten eine "Container-ID"-Eigenschaft, die einen Master-Shape Container identifiziert, dem mit der lokale Eintrag synchronisiert werden muss. Dies kann den Bezeichner eines beliebigen Ordners sein, die Formulare enthält. Dies ist nützlich, wenn Sie einen benutzerdefiniertes Formular-Manager verwenden, der eine Art von organisationsweiten Formularbibliothek unterstützt. der Formular-Manager würde übernehmen synchronisieren die Formulare in der persönlichen Formularbibliothek und der gesamten Organisation Formularbibliothek gespeichert. Dies würde wahrscheinlich vorkommen, wenn der Formular-Manager geladen wurde, jedoch kann jederzeit theoretisch vorkommen.
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

