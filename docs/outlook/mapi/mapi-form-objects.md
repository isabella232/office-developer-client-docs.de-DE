---
title: MAPI-Formularobjekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2802cba7fb9933ba55bf5a064691475caf90b109
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584129"
---
# <a name="mapi-form-objects"></a>MAPI-Formularobjekte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Formularobjekte werden dynamisch von Formularservern erstellt, um bestimmte Nachrichten anzuzeigen und Benutzern die Interaktion mit ihnen zu ermöglichen. Ein Formularobjekt ist daher eine Instanziierung der von [IMAPIForm](imapiformiunknown.md) abgeleiteten Klasse, die vom Formularserver implementiert wird. Wenn eine Clientanwendung eine Nachricht öffnet, erstellt der Formularserver für diese Nachrichtenklasse ein Formularobjekt zum Behandeln der Nachricht. Das Formularobjekt erstellt dann seine Schnittstelle und zeigt die Eigenschaften der Nachricht darin an. Das Formularobjekt und seine Benutzeroberfläche bleiben erhalten, bis der Benutzer es schließt. Das Formularobjekt verarbeitet alle Änderungen an den Werten der Eigenschaften der Nachricht. 
  
Darüber hinaus definieren die MAPI-Formularschnittstellen einen Mechanismus, mit dem ein Formularobjekt eine Reihe von Nachrichten laden und anzeigen kann. Dies ist ein Effizienzmechanismus, da dadurch unnötige Zerstörung und Erstellung von Nachrichtenobjekten und deren Schnittstellen vermieden wird. Wenn der Nachrichtenclient aufgefordert wird, eine andere Nachricht zu laden, sollte das Formularobjekt alle Änderungen an den Eigenschaften der aktuellen Nachricht speichern.
  
Informationen zur Perspektive einer Clientanwendung für Formularobjekte finden Sie unter [MAPI Custom Form Objects](mapi-custom-form-objects.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

