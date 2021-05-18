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
# <a name="mapi-form-objects"></a><span data-ttu-id="a1fce-103">MAPI-Formularobjekte</span><span class="sxs-lookup"><span data-stu-id="a1fce-103">MAPI Form Objects</span></span>

  
  
<span data-ttu-id="a1fce-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1fce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1fce-105">Formularobjekte werden dynamisch von Formularservern erstellt, um bestimmte Nachrichten anzeigen und Benutzern die Interaktion mit diesen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a1fce-105">Form objects are created dynamically by form servers in order to display specific messages and allow users to interact with them.</span></span> <span data-ttu-id="a1fce-106">Ein Formularobjekt ist daher eine Instanziierung der von [IMAPIForm](imapiformiunknown.md) abgeleiteten Klasse, die vom Formularserver implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="a1fce-106">A form object is, therefore, an instantiation of the class derived from [IMAPIForm](imapiformiunknown.md) that is implemented by the form server.</span></span> <span data-ttu-id="a1fce-107">Wenn eine Clientanwendung eine Nachricht öffnet, erstellt der Formularserver für diese Nachrichtenklasse ein Formularobjekt zur Verarbeitung der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a1fce-107">When a client application opens a message, the form server for that message class creates a form object to handle the message.</span></span> <span data-ttu-id="a1fce-108">Das Formularobjekt erstellt dann seine Schnittstelle und zeigt die Eigenschaften der Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="a1fce-108">The form object then creates its interface and displays the properties of the message in it.</span></span> <span data-ttu-id="a1fce-109">Das Formularobjekt und seine Schnittstelle bleiben erhalten, bis der Benutzer es schließt.</span><span class="sxs-lookup"><span data-stu-id="a1fce-109">The form object and its interface persists until the user closes it.</span></span> <span data-ttu-id="a1fce-110">Das Formularobjekt behandelt alle Änderungen an den Werten der Nachrichteneigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1fce-110">The form object handles any changes to the values of the message's properties.</span></span> 
  
<span data-ttu-id="a1fce-111">Darüber hinaus definieren die MAPI-Formularschnittstellen einen Mechanismus, mit dem ein Formularobjekt eine Reihe von Nachrichten laden und anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="a1fce-111">Additionally, the MAPI form interfaces define a mechanism by which one form object can load and display a series of messages.</span></span> <span data-ttu-id="a1fce-112">Dies ist ein Effizienzmechanismus, da er unnötige Zerstörung und Erstellung von Nachrichtenobjekten und deren Schnittstellen verhindert.</span><span class="sxs-lookup"><span data-stu-id="a1fce-112">This is an efficiency mechanism, as it avoids needless destruction and creation of message objects and their interfaces.</span></span> <span data-ttu-id="a1fce-113">Wenn der Messagingclient aufgefordert wird, eine andere Nachricht zu laden, sollte das Formularobjekt alle Änderungen an den Eigenschaften der aktuellen Nachricht speichern.</span><span class="sxs-lookup"><span data-stu-id="a1fce-113">When requested by the messaging client to load a different message, the form object should save any changes to the current message's properties.</span></span>
  
<span data-ttu-id="a1fce-114">Informationen zur Perspektive einer Clientanwendung auf Formularobjekte finden Sie unter [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a1fce-114">For information on a client application's perspective of form objects, see [MAPI Custom Form Objects](mapi-custom-form-objects.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a1fce-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1fce-115">See also</span></span>



[<span data-ttu-id="a1fce-116">MAPI-Formulare</span><span class="sxs-lookup"><span data-stu-id="a1fce-116">MAPI Forms</span></span>](mapi-forms.md)

