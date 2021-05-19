---
title: Entwickeln von MAPI-Formularservern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420766"
---
# <a name="developing-mapi-form-servers"></a><span data-ttu-id="b758b-103">Entwickeln von MAPI-Formularservern</span><span class="sxs-lookup"><span data-stu-id="b758b-103">Developing MAPI Form Servers</span></span>

  
  
<span data-ttu-id="b758b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b758b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b758b-105">In diesem Abschnitt wird das Erstellen ausführbarer Und Formularkonfigurationsdateien für formularserver zum Erstellen benutzerdefinierter MAPI-Formulare beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b758b-105">This section describes the process of creating form server executable and form configuration files for creating custom MAPI forms.</span></span> <span data-ttu-id="b758b-106">Bevor Sie diesen Abschnitt lesen, sollten Sie sich mit den Informationen in [MAPI Forms vertraut machen.](mapi-forms.md)</span><span class="sxs-lookup"><span data-stu-id="b758b-106">Before reading this section, you should familiarize yourself with the information in [MAPI Forms](mapi-forms.md).</span></span>
  
<span data-ttu-id="b758b-107">Die Entwicklung eines Formularservers umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="b758b-107">Developing a form server includes the following steps:</span></span>
  
1. <span data-ttu-id="b758b-108">Entscheiden Sie, welche Informationen das Formular enthalten soll, und wählen Sie einen Satz von Eigenschaften aus, um diese Informationen zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="b758b-108">Deciding what information the form will contain and choosing a set of properties to hold that information.</span></span> <span data-ttu-id="b758b-109">Weitere Informationen finden Sie [unter Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="b758b-109">For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).</span></span>
    
2. <span data-ttu-id="b758b-110">Entwerfen einer Benutzeroberfläche, mit der Benutzer mit den Eigenschaften des Formulars interagieren können.</span><span class="sxs-lookup"><span data-stu-id="b758b-110">Designing a user interface with which users can interact with the form's properties.</span></span>
    
3. <span data-ttu-id="b758b-111">Auswählen einer Nachrichtenklasse und Generieren einer eindeutigen Klassen-ID (CLSID).</span><span class="sxs-lookup"><span data-stu-id="b758b-111">Choosing a message class and generating a unique class identifier (CLSID).</span></span> <span data-ttu-id="b758b-112">Eine Übersicht über Nachrichtenklassen finden Sie unter [MAPI Message Classes](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="b758b-112">For an overview of message classes, see [MAPI Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="b758b-113">Weitere Informationen zu Nachrichtenklassen und Formularen finden Sie unter [Choosing a Message Class](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="b758b-113">For more information about message classes and forms, see [Choosing a Message Class](choosing-a-message-class.md).</span></span>
    
4. <span data-ttu-id="b758b-114">Implementieren der erforderlichen MAPI-Formularschnittstellen sowie optionaler Schnittstellen, die Ihr bestimmter Formularserver benötigt.</span><span class="sxs-lookup"><span data-stu-id="b758b-114">Implementing the required MAPI form interfaces, as well as any optional interfaces that your particular form server needs.</span></span> <span data-ttu-id="b758b-115">Weitere Informationen finden Sie unter [Writing Form Server Code](writing-form-server-code.md).</span><span class="sxs-lookup"><span data-stu-id="b758b-115">For more information, see [Writing Form Server Code](writing-form-server-code.md).</span></span> 
    
5. <span data-ttu-id="b758b-116">Schreiben von Benutzeroberflächencode zur Verarbeitung der Benutzerinteraktion mit dem Formularobjekt und den vom Formular verwendeten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b758b-116">Writing user interface code to handle the user's interaction with the form object and the properties the form uses.</span></span>
    
6. <span data-ttu-id="b758b-117">Erstellen einer Formularkonfigurationsdatei für das Formular.</span><span class="sxs-lookup"><span data-stu-id="b758b-117">Creating a form configuration file for the form.</span></span> <span data-ttu-id="b758b-118">Weitere Informationen finden Sie [unter Dateiformat von Formularkonfigurationsdateien](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="b758b-118">For more information, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
    
7. <span data-ttu-id="b758b-119">Installieren des Formulars auf den Computern der Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b758b-119">Installing the form on users' computers.</span></span> <span data-ttu-id="b758b-120">Weitere Informationen finden Sie unter [Installing a Form into a Library](installing-a-form-into-a-library.md).</span><span class="sxs-lookup"><span data-stu-id="b758b-120">For more information, see [Installing a Form into a Library](installing-a-form-into-a-library.md).</span></span>
    
<span data-ttu-id="b758b-121">Wahrscheinlich führen Sie die Schritte 1 bis 5 gleichzeitig aus, anstatt sie in der Reihenfolge durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="b758b-121">You will most likely perform steps 1 through 5 simultaneously rather than completing them in sequence.</span></span> <span data-ttu-id="b758b-122">Der Prozess der Entwicklung eines Formularservers ist wie viele Programmierprojekte kein Prozess, in dem eine besonders definierte Sequenz vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b758b-122">The process of developing a form server, like many programming projects, is not one in which there is a particularly well-defined sequence.</span></span> <span data-ttu-id="b758b-123">Das Erstellen einer Formularkonfigurationsdatei wird z. B. als vorletzter Schritt angezeigt, Aber Sie erstellen ihre Formularkonfigurationsdatei wahrscheinlich inkrementell, und sie wird vollständiger, wenn Sie Dem Formularserver Features hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b758b-123">For example, creating a form configuration file is shown as the second-to-last step above, but you will probably create your form configuration file incrementally, and it will become more complete as you add features to your form server.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b758b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b758b-124">See also</span></span>



[<span data-ttu-id="b758b-125">MAPI-Konzepte (engl.)</span><span class="sxs-lookup"><span data-stu-id="b758b-125">MAPI Concepts</span></span>](mapi-concepts.md)

