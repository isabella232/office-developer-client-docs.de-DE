---
title: MAPI-Formularobjekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb9107d9-ad5c-4264-a457-dea193597dc9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5a7c6c575f277a91a18f0d834e26d3d376613fba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404785"
---
# <a name="mapi-form-objects"></a>MAPI-Formularobjekte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Formularobjekte werden dynamisch von Formularservern erstellt, um bestimmte Nachrichten anzeigen und Benutzern die Interaktion mit diesen zu ermöglichen. Ein Formularobjekt ist daher eine Instanziierung der von [IMAPIForm](imapiformiunknown.md) abgeleiteten Klasse, die vom Formularserver implementiert wird. Wenn eine Clientanwendung eine Nachricht öffnet, erstellt der Formularserver für diese Nachrichtenklasse ein Formularobjekt zur Verarbeitung der Nachricht. Das Formularobjekt erstellt dann seine Schnittstelle und zeigt die Eigenschaften der Nachricht an. Das Formularobjekt und seine Schnittstelle bleiben erhalten, bis der Benutzer es schließt. Das Formularobjekt behandelt alle Änderungen an den Werten der Nachrichteneigenschaften. 
  
Darüber hinaus definieren die MAPI-Formularschnittstellen einen Mechanismus, mit dem ein Formularobjekt eine Reihe von Nachrichten laden und anzeigen kann. Dies ist ein Effizienzmechanismus, da er unnötige Zerstörung und Erstellung von Nachrichtenobjekten und deren Schnittstellen verhindert. Wenn der Messagingclient aufgefordert wird, eine andere Nachricht zu laden, sollte das Formularobjekt alle Änderungen an den Eigenschaften der aktuellen Nachricht speichern.
  
Informationen zur Perspektive einer Clientanwendung auf Formularobjekte finden Sie unter [MAPI Custom Form Objects](mapi-custom-form-objects.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

