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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351464"
---
# <a name="mapi-form-objects"></a>MAPI-Formularobjekte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Formularobjekte werden von Formular Servern dynamisch erstellt, um bestimmte Nachrichten anzuzeigen und Benutzern die Interaktion mit diesen zu ermöglichen. Ein Form-Objekt ist daher eine Instanziierung der von [IMAPIForm](imapiformiunknown.md) abgeleiteten Klasse, die vom Formularserver implementiert wird. Wenn eine Clientanwendung eine Nachricht öffnet, erstellt der Formularserver für diese Nachrichtenklasse ein Form-Objekt zur Behandlung der Nachricht. Das Form-Objekt erstellt dann seine Schnittstelle und zeigt die Eigenschaften der Nachricht darin an. Das Form-Objekt und seine Schnittstelle bleiben erhalten, bis der Benutzer Sie schließt. Das Form-Objekt behandelt alle Änderungen an den Werten der Eigenschaften der Nachricht. 
  
Darüber hinaus definieren die MAPI-Formular Schnittstellen einen Mechanismus, mit dem ein Form-Objekt geladen und eine Reihe von Nachrichten angezeigt werden kann. Hierbei handelt es sich um einen Effizienz Mechanismus, da dadurch die unnötige Zerstörung und die Erstellung von Nachrichtenobjekten und deren Schnittstellen vermieden werden. Wenn vom Messaging Client eine andere Nachricht geladen wird, sollte das Form-Objekt alle Änderungen an den Eigenschaften der aktuellen Nachricht speichern.
  
Informationen zur Perspektive einer Clientanwendung für Formularobjekte finden Sie unter [MAPI Custom Form Objects](mapi-custom-form-objects.md).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

