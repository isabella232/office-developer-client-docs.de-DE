---
title: MAPI-Formular-Objekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 426d3d5787f4ef8cde2883c5e2eb3699dd664965
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792996"
---
# <a name="mapi-form-objects"></a>MAPI-Formular-Objekte

  
  
**Betrifft**: Outlook 
  
Formular-Objekte werden von Servern, um bestimmte Nachrichten anzeigen und zulassen, dass Benutzer mit ihnen interagieren Formular dynamisch erstellt. Ein Form-Objekt ist daher eine Instanziierung der abgeleiteten Klasse von [IMAPIForm](imapiformiunknown.md) , die vom Formular Server implementiert wird. Wenn eine Nachricht von eine anderen Clientanwendung geöffnet wird, erstellt der Formular-Server für die Nachrichtenklasse ein Form-Objekt, um die Meldung zu behandeln. Das Form-Objekt klicken Sie dann die Benutzeroberfläche erstellt und zeigt die Eigenschaften der Nachricht darin. Das Form-Objekt und seine Schnittstelle bleibt bestehen, bis der Benutzer geschlossen wird. Das Form-Objekt verarbeitet Änderungen an die Werte der Eigenschaften der Nachricht. 
  
Darüber hinaus definieren die Schnittstellen im MAPI-Formulars einen Mechanismus, mit dem ein Form-Objekt geladen und eine Reihe von Nachrichten angezeigt. Dies ist ein Mechanismus Effizienz, wie diese Erstellung der Nachrichtenobjekte und ihre Schnittstellen und unnötige Vernichtung vermieden wird. Auf Anforderung durch die messaging-Client eine andere Meldung geladen werden, sollte das Form-Objekt alle Änderungen auf die aktuelle Nachricht Eigenschaften zu speichern.
  
Informationen zu einer Clientanwendung aus Sicht des Formular-Objekte finden Sie unter [MAPI benutzerdefinierte Formular-Objekte](mapi-custom-form-objects.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

