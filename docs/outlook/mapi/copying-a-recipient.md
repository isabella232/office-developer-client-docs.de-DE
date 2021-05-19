---
title: Kopieren eines Empfängers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3a4fb1a3f76481bf1960c251a33911b871a8791c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419086"
---
# <a name="copying-a-recipient"></a><span data-ttu-id="7f582-103">Kopieren eines Empfängers</span><span class="sxs-lookup"><span data-stu-id="7f582-103">Copying a Recipient</span></span>

  
  
<span data-ttu-id="7f582-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f582-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f582-105">Um einen oder mehrere Empfänger aus einem Container in einen anderen oder denselben Container zu kopieren, überprüfen Sie zunächst, ob der Zielcontainer veränderbar ist.</span><span class="sxs-lookup"><span data-stu-id="7f582-105">To copy one or more recipients from one container into another or the same container, first check that the target container is modifiable.</span></span> <span data-ttu-id="7f582-106">Container, die veränderbar sind, legen AB_MODIFIABLE -Flag in ihrer **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="7f582-106">Containers that are modifiable set the AB_MODIFIABLE flag in their **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="7f582-107">Um einen oder mehrere Einträge in einen veränderbaren Container zu kopieren, rufen Sie die [IABContainer::CopyEntries-Methode des Zielcontainers](iabcontainer-copyentries.md) auf.</span><span class="sxs-lookup"><span data-stu-id="7f582-107">To copy one or more entries into a modifiable container, call the destination container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method.</span></span> <span data-ttu-id="7f582-108">Da das Kopieren von Adressbucheinträgen zeitaufwändig sein kann, akzeptiert **CopyEntries** vier Eingabeparameter: ein Array von Eingabebezeichnern für die zu kopierenden Einträge, ein Fensterhandle, eine Statusanzeige und eine Bitmaske mit Flags.</span><span class="sxs-lookup"><span data-stu-id="7f582-108">Because copying address book entries can be time-consuming, **CopyEntries** accepts four input parameters: an array of entry identifiers for the entries to be copied, a window handle, a progress indicator, and a bitmask of flags.</span></span> 
  
<span data-ttu-id="7f582-109">Das Fensterhandle und die Statusanzeige werden vom Adressbuchanbieter verwendet, um dem Benutzer den Status des Vorgangs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7f582-109">The window handle and progress indicator are used by the address book provider to show the status of the operation to the user.</span></span> <span data-ttu-id="7f582-110">Wenn Sie den Fortschritt anzeigen möchten, übergeben Sie ein Fensterhandle für das übergeordnete Fenster der Statusanzeige im _ulUIParam-Parameter,_ und legen Sie nicht das AB_NO_DIALOG im _ulFlags-Parameter._</span><span class="sxs-lookup"><span data-stu-id="7f582-110">If you want to display progress, pass a window handle for the parent window of the progress indicator in the  _ulUIParam_ parameter and do not set the AB_NO_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="7f582-111">Wenn Sie über eine eigene Implementierung eines Fortschrittsindikators verfügen, übergeben Sie einen Zeiger auf die Implementierung im _lpProgress-Parameter._</span><span class="sxs-lookup"><span data-stu-id="7f582-111">If you have your own implementation of a progress indicator, pass a pointer to the implementation in the  _lpProgress_ parameter.</span></span> <span data-ttu-id="7f582-112">Wenn nicht, übergeben Sie NULL.</span><span class="sxs-lookup"><span data-stu-id="7f582-112">If not, pass NULL.</span></span> <span data-ttu-id="7f582-113">Der Adressbuchanbieter verwendet die Implementierung des MAPI-Fortschrittsindikators.</span><span class="sxs-lookup"><span data-stu-id="7f582-113">The address book provider will use the MAPI progress indicator implementation.</span></span> 
  
<span data-ttu-id="7f582-114">Die Bitmaske der Flags gibt an, ob sie eine Statusanzeige anzeigen möchten und wie die Überprüfung doppelter Einträge behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f582-114">The bitmask of flags indicates whether or not you want to display a progress indicator and how duplicate entry checking should be handled.</span></span> <span data-ttu-id="7f582-115">Legen Sie das AB_NO_DIALOG, um eine Statusanzeige zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="7f582-115">Set the AB_NO_DIALOG flag to suppress a progress indicator.</span></span> <span data-ttu-id="7f582-116">Legen Sie CREATE_CHECK_DUP_LOOSE,um den Adressbuchanbieter anweisen, auf Duplikate oder das CREATE_CHECK_DUP_STRICT auf eine strengere Duplikatprüfung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7f582-116">Set the CREATE_CHECK_DUP_LOOSE flag to instruct the address book provider to loosely check for duplicates or the CREATE_CHECK_DUP_STRICT flag for stricter duplicate checking.</span></span> <span data-ttu-id="7f582-117">Legen Sie CREATE_REPLACE, dass kopierte Einträge vorhandene Einträge ersetzen, wenn der Anbieter feststellt, dass Duplikate vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7f582-117">Set the CREATE_REPLACE flag to have copied entries replace existing entries when the provider determines there are duplicates.</span></span> 
  
<span data-ttu-id="7f582-118">Beim Kopieren in einen persönlichen Adressbuchcontainer kopiert der Anbieter einige oder alle Eigenschaften für jeden Eintrag.</span><span class="sxs-lookup"><span data-stu-id="7f582-118">When copying into a personal address book (PAB) container, the provider copies some or all of the properties for each entry.</span></span> <span data-ttu-id="7f582-119">Da MAPI keine Anforderungen für Anbieter mit Containerkopievorgängen stellt, können Sie keine Annahmen über die Anzahl und den Typ der Eigenschaften machen, die mit einem Adressbucheintrag kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="7f582-119">Because MAPI does not establish requirements for providers implementing container copy operations, you cannot make assumptions about the number and type of properties that are copied with an address book entry.</span></span>
  

