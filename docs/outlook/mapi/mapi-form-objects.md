---
title: MAPI-Formular-Objekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0cece598d4ad337e29edb3bb98b302de900e056d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593466"
---
# <a name="mapi-form-objects"></a>MAPI-Formular-Objekte

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Formular-Objekte werden von Servern, um bestimmte Nachrichten anzeigen und zulassen, dass Benutzer mit ihnen interagieren Formular dynamisch erstellt. Ein Form-Objekt ist daher eine Instanziierung der abgeleiteten Klasse von [IMAPIForm](imapiformiunknown.md) , die vom Formular Server implementiert wird. Wenn eine Nachricht von eine anderen Clientanwendung geöffnet wird, erstellt der Formular-Server für die Nachrichtenklasse ein Form-Objekt, um die Meldung zu behandeln. Das Form-Objekt klicken Sie dann die Benutzeroberfläche erstellt und zeigt die Eigenschaften der Nachricht darin. Das Form-Objekt und seine Schnittstelle bleibt bestehen, bis der Benutzer geschlossen wird. Das Form-Objekt verarbeitet Änderungen an die Werte der Eigenschaften der Nachricht. 
  
Darüber hinaus definieren die Schnittstellen im MAPI-Formulars einen Mechanismus, mit dem ein Form-Objekt geladen und eine Reihe von Nachrichten angezeigt. Dies ist ein Mechanismus Effizienz, wie diese Erstellung der Nachrichtenobjekte und ihre Schnittstellen und unnötige Vernichtung vermieden wird. Auf Anforderung durch die messaging-Client eine andere Meldung geladen werden, sollte das Form-Objekt alle Änderungen auf die aktuelle Nachricht Eigenschaften zu speichern.
  
Informationen zu einer Clientanwendung aus Sicht des Formular-Objekte finden Sie unter [MAPI benutzerdefinierte Formular-Objekte](mapi-custom-form-objects.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

