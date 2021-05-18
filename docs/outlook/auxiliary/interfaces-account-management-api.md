---
title: Schnittstellen (Kontoverwaltungs-API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e67b0690-a3f4-4523-94a6-c0e4005bcb69
description: In diesem Abschnitt werden die Schnittstellen in der Kontoverwaltungs-API beschrieben.
ms.openlocfilehash: 31685e0fe04d0b72315a13c2f80fcb0fffc72a82
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319250"
---
# <a name="interfaces-account-management-api"></a><span data-ttu-id="b469f-103">Schnittstellen (Kontoverwaltungs-API)</span><span class="sxs-lookup"><span data-stu-id="b469f-103">Interfaces (Account management API)</span></span>

<span data-ttu-id="b469f-104">In diesem Abschnitt werden die Schnittstellen in der Kontoverwaltungs-API beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b469f-104">This section describes the interfaces in the Account Management API.</span></span>
  
|<span data-ttu-id="b469f-105">**Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b469f-105">**Interface**</span></span>|<span data-ttu-id="b469f-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b469f-106">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b469f-107">IOlkAccount</span><span class="sxs-lookup"><span data-stu-id="b469f-107">IOlkAccount</span></span>](iolkaccount.md) <br/> |<span data-ttu-id="b469f-108">Unterstützt das Abrufen und Festlegen von Eigenschaften und anderen Informationen zu einem Konto.</span><span class="sxs-lookup"><span data-stu-id="b469f-108">Supports getting and setting of properties and other information about an account.</span></span>  <br/> |
|[<span data-ttu-id="b469f-109">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="b469f-109">IOlkAccountHelper</span></span>](iolkaccounthelper.md) <br/> |<span data-ttu-id="b469f-110">Stellt Hilfsfunktionen in der aktuellen MAPI-Sitzung zum Verwalten von Konten bereit.</span><span class="sxs-lookup"><span data-stu-id="b469f-110">Provides helper functionality in the current MAPI session to manage accounts.</span></span>  <br/> |
|[<span data-ttu-id="b469f-111">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="b469f-111">IOlkAccountManager</span></span>](iolkaccountmanager.md) <br/> |<span data-ttu-id="b469f-112">Verwaltet den Zugriff auf Konten und richtet Benachrichtigungen zu Kontoänderungen ein.</span><span class="sxs-lookup"><span data-stu-id="b469f-112">Manages access to accounts and sets up notifications about account changes.</span></span>  <br/> |
|[<span data-ttu-id="b469f-113">IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="b469f-113">IOlkAccountNotify</span></span>](iolkaccountnotify.md) <br/> |<span data-ttu-id="b469f-114">Stellt einen Rückruf an den Client für Änderungen an einem Konto.</span><span class="sxs-lookup"><span data-stu-id="b469f-114">Provides a callback to the client for changes to an account.</span></span>  <br/> |
|[<span data-ttu-id="b469f-115">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="b469f-115">IOlkEnum</span></span>](iolkenum.md) <br/> |<span data-ttu-id="b469f-116">Unterstützt das Aufzählen von Konten als [IUnknown-Objekte.](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="b469f-116">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span>  <br/> |
|[<span data-ttu-id="b469f-117">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="b469f-117">IOlkErrorUnknown</span></span>](iolkerrorunknown.md) <br/> |<span data-ttu-id="b469f-118">Stellt zusätzliche Informationen zum letzten Fehler zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b469f-118">Provides extra information about the last error.</span></span>  <br/> |
   

