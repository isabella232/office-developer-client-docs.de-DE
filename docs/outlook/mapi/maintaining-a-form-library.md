---
title: Verwalten einer Formularbibliothek
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 51c7c3f8ba70dcb3d35dc50806e984fd4b193818
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408803"
---
# <a name="maintaining-a-form-library"></a><span data-ttu-id="63b2f-103">Verwalten einer Formularbibliothek</span><span class="sxs-lookup"><span data-stu-id="63b2f-103">Maintaining a Form Library</span></span>

  
  
<span data-ttu-id="63b2f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63b2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63b2f-105">Eine Formularbibliothek enthält alle wichtigen Informationen zu einem Formular: seine Eigenschaften, Verben und ausführbaren Dateien des Servers.</span><span class="sxs-lookup"><span data-stu-id="63b2f-105">A form library holds all of the important information about a form: its properties, its verbs, and its server's executable files.</span></span> <span data-ttu-id="63b2f-106">Einige Clients ermöglichen benutzern das Warten, Installieren oder Entfernen von Formularservern.</span><span class="sxs-lookup"><span data-stu-id="63b2f-106">Some clients allow their users to maintain, install, or remove form servers.</span></span> <span data-ttu-id="63b2f-107">Wenn Sie diese Funktion Ihren Benutzern anbieten möchten, müssen Sie Zugriff auf:</span><span class="sxs-lookup"><span data-stu-id="63b2f-107">If you want to offer this feature to your users, you must have access to:</span></span>
  
- <span data-ttu-id="63b2f-108">Die Konfigurationsdatei des Formularservers, eine Datei mit dem . CFG-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="63b2f-108">The form server's configuration file, a file with the .CFG extension.</span></span>
    
- <span data-ttu-id="63b2f-109">Das Containerobjekt der Formularbibliothek, ein Objekt, das die [IMAPIFormContainer : IUnknown-Schnittstelle](imapiformcontaineriunknown.md) implementiert.</span><span class="sxs-lookup"><span data-stu-id="63b2f-109">The form library's container object, an object that implements the [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
<span data-ttu-id="63b2f-110">Um auf die Konfigurationsdatei oder einen Pfadnamen zu dieser zu zugreifen, verwenden Sie die praktischen Mittel.</span><span class="sxs-lookup"><span data-stu-id="63b2f-110">To access the configuration file or a pathname to it, use whatever means are convenient.</span></span> <span data-ttu-id="63b2f-111">In der Regel stellen Clients dem Benutzer ein Dialogfeld zum Installieren und Entfernen von Formularservern vor, das auch verwendet werden kann, um den Benutzer zum Speicherort der Konfigurationsdatei aufforderen.</span><span class="sxs-lookup"><span data-stu-id="63b2f-111">Usually, clients present the user with a dialog box for installing and removing form servers that can also be used to prompt the user for the location of the configuration file.</span></span>
  
<span data-ttu-id="63b2f-112">Um auf den Container der Formularbibliothek zu zugreifen, rufen Sie die [IMAPIFormMgr::OpenFormContainer-Methode](imapiformmgr-openformcontainer.md) des Formular-Managers auf.</span><span class="sxs-lookup"><span data-stu-id="63b2f-112">To access the form library's container, call the form manager's [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method.</span></span> <span data-ttu-id="63b2f-113">Übergeben Sie einen Enumerationswert, um anzugeben, welche Formularbibliothek geöffnet werden soll, und gegebenenfalls einen Zeiger auf das Objekt, mit dem der Formular-Manager die Formularbibliothek öffnen soll.</span><span class="sxs-lookup"><span data-stu-id="63b2f-113">Pass in an enumeration value to specify which form library to open, and if necessary, a pointer to the object that the form manager should use to open the form library.</span></span> <span data-ttu-id="63b2f-114">Wenn Sie beispielsweise eine Ordnerformularbibliothek [öffnen,](folder-form-libraries.md)übergeben Sie einen [IMAPIFolder : IMAPIContainer-Zeiger.](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="63b2f-114">For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer.</span></span> 
  
<span data-ttu-id="63b2f-115">Nachdem **OpenFormContainer** den **IMAPIFormContainer-Zeiger** zurückgegeben hat, rufen Sie [entweder IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) oder [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md)auf, je nachdem, wie die Wartung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="63b2f-115">After **OpenFormContainer** returns the **IMAPIFormContainer** pointer, call either [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) or [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), depending on the maintenance to be performed.</span></span> <span data-ttu-id="63b2f-116">**InstallForm** fügt der Bibliothek einen Formularserver hinzu. **RemoveForm** löscht einen Formularserver aus der Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="63b2f-116">**InstallForm** adds a form server to the library; **RemoveForm** deletes a form server from the library.</span></span> 
  

