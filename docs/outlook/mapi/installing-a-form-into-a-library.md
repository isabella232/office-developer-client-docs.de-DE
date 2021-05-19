---
title: Installieren eines Formulars in einer Bibliothek
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 08470a80153e42136922ae502252d83de0125512
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433143"
---
# <a name="installing-a-form-into-a-library"></a><span data-ttu-id="7d3e6-103">Installieren eines Formulars in einer Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7d3e6-103">Installing a Form into a Library</span></span>

  
  
<span data-ttu-id="7d3e6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d3e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d3e6-105">Der standardmäßige MAPI-Formular-Manager, der mit dem Windows SDK bereitgestellt wird, stellt keine Benutzeroberfläche zum Installieren von Formularen in den verschiedenen Formularbibliotheken bereit.</span><span class="sxs-lookup"><span data-stu-id="7d3e6-105">The default MAPI form manager supplied with the Windows SDK does not provide a user interface for installing forms in the various form libraries.</span></span> <span data-ttu-id="7d3e6-106">Aus diesem Grund müssen Sie eine kleine Anwendung oder detaillierte Anweisungen erstellen, die Benutzer zum Installieren des Formulars verwenden können.</span><span class="sxs-lookup"><span data-stu-id="7d3e6-106">Because of this, you will have to create a small application — or detailed set of instructions — that users can use to install the form.</span></span>
  
<span data-ttu-id="7d3e6-107">Wenn Sie eine Installationsanwendung implementieren, sind die folgenden Aktionen erforderlich, um ein Formular in der zugehörigen Inhaltstabelle eines Ordners zu installieren:</span><span class="sxs-lookup"><span data-stu-id="7d3e6-107">If you implement an installation application, the series of actions it must perform to install a form into a folder's associated contents table are as follows:</span></span>
  
1. <span data-ttu-id="7d3e6-108">Rufen Sie die [MAPIOpenFormMgr-Funktion](mapiopenformmgr.md) auf, um den Formular-Manager zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7d3e6-108">Call the [MAPIOpenFormMgr](mapiopenformmgr.md) function to open the form manager.</span></span> 
    
2. <span data-ttu-id="7d3e6-109">Verwenden [Sie die IMAPIFormMgr::OpenFormContainer-](imapiformmgr-openformcontainer.md) oder [IMAPIFormMgr::SelectFormContainer-Methode,](imapiformmgr-selectformcontainer.md) um den Zielcontainer für das Formular auszuwählen und zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="7d3e6-109">Use [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) or [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to select and open the target container for the form.</span></span> 
    
3. <span data-ttu-id="7d3e6-110">Verwenden Sie die [IMAPIFormContainer::InstallForm-Funktion,](imapiformcontainer-installform.md) um das Formular zu installieren.</span><span class="sxs-lookup"><span data-stu-id="7d3e6-110">Use the [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) function to install the form.</span></span> 
    
    <span data-ttu-id="7d3e6-111">Die Schritte 4 bis 6 sind für die Installation in einer lokalen Formularbibliothek:</span><span class="sxs-lookup"><span data-stu-id="7d3e6-111">Steps 4 through 6 are for installation into a local form library:</span></span>
    
4. <span data-ttu-id="7d3e6-112">Kopieren Sie alle Dateien an den entsprechenden Ort auf dem lokalen Datenträger, wenn die Installation in der lokalen Formularbibliothek auf der Arbeitsstation des Benutzers erfolgt.</span><span class="sxs-lookup"><span data-stu-id="7d3e6-112">Copy all files to the appropriate place on the local disk, if installation is to the local form library on the user's workstation.</span></span> <span data-ttu-id="7d3e6-113">Ändern Sie bei Bedarf die Formularkonfigurationsdatei, um die aktuellen Pfade von Komponenten widerspiegeln zu können.</span><span class="sxs-lookup"><span data-stu-id="7d3e6-113">If necessary, modify the form configuration file to reflect current paths of components.</span></span> <span data-ttu-id="7d3e6-114">Die Formularkonfigurationsdatei kann relative Pfade enthalten, in diesem Fall ist dieser Schritt möglicherweise nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7d3e6-114">The form configuration file can contain relative paths, in which case this step may not be necessary.</span></span>
    
5. <span data-ttu-id="7d3e6-115">Führen Sie die entsprechenden OLE-Registrierungsschritte aus, um den Nachrichtentyp dem zu installierende Formularserver zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="7d3e6-115">Complete the appropriate OLE registration steps to associate the message type with the form server being installed.</span></span>
    
6. <span data-ttu-id="7d3e6-116">Wenn das Formular in der lokalen Formularbibliothek installiert wurde, kopieren Sie das Symbol (.ico) und die Konfigurationsdateien (CFG) des Formulars in das Verzeichnis %WINDOWS%\FORMS\CONFIGS, damit das Formular automatisch wiederhergestellt werden kann, falls die Formularbibliothek beschädigt oder gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="7d3e6-116">If the form was installed into the local form library, copy the form's icon (.ico) and configuration (.cfg) files into the %WINDOWS%\FORMS\CONFIGS directory so the form can be automatically restored in case the form library is corrupted or deleted.</span></span> <span data-ttu-id="7d3e6-117">Dieser Schritt wird empfohlen, ist jedoch nicht zwingend erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7d3e6-117">This step is recommended but not mandatory.</span></span>
    
> [!NOTE]
> <span data-ttu-id="7d3e6-118">Sie können die Installation in einer lokalen Formularbibliothek vereinfachen, indem Sie die Schritte 1 und 2 durch einen Aufruf der [MAPIOpenLocalFormContainer-Funktion](mapiopenlocalformcontainer.md) ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7d3e6-118">You can simplify installation to a local form library by replacing steps 1 and 2 with a call to the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7d3e6-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d3e6-119">See also</span></span>



[<span data-ttu-id="7d3e6-120">Entwickeln von MAPI-Formularservern</span><span class="sxs-lookup"><span data-stu-id="7d3e6-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

