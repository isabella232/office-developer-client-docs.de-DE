---
title: Steuern der Objektimplementierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b4b225f7e048ef40a79c4b258629cb01b79368d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565830"
---
# <a name="control-object-implementation"></a><span data-ttu-id="50f2f-103">Steuern der Objektimplementierung</span><span class="sxs-lookup"><span data-stu-id="50f2f-103">Control Object Implementation</span></span>

  
  
<span data-ttu-id="50f2f-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50f2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50f2f-105">Steuerelement-Objekte oder Objekte, die unterstützen die [IMAPIControl: IUnknown](imapicontroliunknown.md) Schnittstelle, die implementiert werden, von Anbietern Funktionen eine Schaltfläche hinzu, die in einem MAPI-Dialogfeld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="50f2f-105">Control objects, or objects that support the [IMAPIControl : IUnknown](imapicontroliunknown.md) interface, are implemented by providers to add functionality to a button that appears on a MAPI dialog box.</span></span> <span data-ttu-id="50f2f-106">Control-Objekte können nur für Schaltflächen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="50f2f-106">Control objects can only be implemented for buttons.</span></span> 
  
 <span data-ttu-id="50f2f-107">**IMAPIControl** verfügt über drei Methoden: [GetLastError](imapicontrol-getlasterror.md) [GetState](imapicontrol-getstate.md)und zu [Aktivieren](imapicontrol-activate.md).</span><span class="sxs-lookup"><span data-stu-id="50f2f-107">**IMAPIControl** has three methods: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md), and [Activate](imapicontrol-activate.md).</span></span> 
  
<span data-ttu-id="50f2f-108">MAPI-Aufrufen **GetState** , um zu bestimmen, ob die Schaltfläche zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="50f2f-108">MAPI calls **GetState** to determine whether or not to disable the button.</span></span> <span data-ttu-id="50f2f-109">**GetState** wird in den folgenden Situationen aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="50f2f-109">**GetState** is called in the following situations:</span></span> 
  
- <span data-ttu-id="50f2f-110">Wenn das Dialogfeld, in dem die Schaltfläche angezeigt wird, zuerst angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="50f2f-110">When the dialog box on which the button appears is first displayed.</span></span>
    
- <span data-ttu-id="50f2f-111">Wenn eine Anzeige Tabelle Benachrichtigung für die Schaltfläche ausgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="50f2f-111">When a display table notification is issued for the button.</span></span> 
    
<span data-ttu-id="50f2f-112">Legen Sie den Inhalt des Parameters _LpulState_ auf MAPI_DISABLED, wenn der Benutzer mit der Schaltfläche und MAPI_ENABLED interagieren kann, wenn der Benutzer interagieren kann.</span><span class="sxs-lookup"><span data-stu-id="50f2f-112">Set the contents of the  _lpulState_ parameter to MAPI_DISABLED if the user cannot interact with the button and MAPI_ENABLED if the user can interact.</span></span> 
  
<span data-ttu-id="50f2f-113">Wenn der Benutzer auf die Schaltfläche klickt, ruft MAPI **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="50f2f-113">When the user clicks the button, MAPI calls **Activate**.</span></span> <span data-ttu-id="50f2f-114">**Activate** führt die Aufgabe, die die Schaltfläche zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="50f2f-114">**Activate** performs the task that has been associated with the button.</span></span> <span data-ttu-id="50f2f-115">Für diese Aufgabe kann beliebig für Ihren Anbieter, wie ein Dialogfeld angezeigt, oder Aktualisieren einer Eigenschaft geeignet sein.</span><span class="sxs-lookup"><span data-stu-id="50f2f-115">This task can be anything appropriate for your provider, such as displaying a dialog box or updating a property.</span></span> <span data-ttu-id="50f2f-116">Wenn der Vorgang nicht erfolgreich ist, da der Benutzer den Vorgang abgebrochen, geben Sie MAPI_E_USER_CANCEL zurück.</span><span class="sxs-lookup"><span data-stu-id="50f2f-116">If the task is unsuccessful because the user canceled it, return MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="50f2f-117">Weitere Ursachen des Fehlers den entsprechenden Fehlerwert zurück.</span><span class="sxs-lookup"><span data-stu-id="50f2f-117">For other causes of failure, return the appropriate error value.</span></span> 
  
<span data-ttu-id="50f2f-118">Rufen Sie [ITableData::HrNotify](itabledata-hrnotify.md), wenn der Vorgang erfolgreich ist und mit einer Änderung der Eigenschaft, die in ein anderes Steuerelement im Dialogfeld wiedergegeben wird verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="50f2f-118">If the task is successful and it is linked to a property change that is reflected in another control on the dialog box, call [ITableData::HrNotify](itabledata-hrnotify.md).</span></span> <span data-ttu-id="50f2f-119">**HrNotify** wird aufgerufen, um eine Anzeige Tabelle Benachrichtigung mit der geänderten **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md))-Eigenschaft in der Struktur [TABLE_NOTIFICATION](table_notification.md) Problem.</span><span class="sxs-lookup"><span data-stu-id="50f2f-119">**HrNotify** is called to issue a display table notification with the changed property's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> <span data-ttu-id="50f2f-120">Setzen Sie den neuen Eigenschaftswert nicht in der Struktur. Stattdessen geben sie zurück, wenn [IMAPIProp::GetProps](imapiprop-getprops.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="50f2f-120">Do not place the new property value in the structure; instead, return it when [IMAPIProp::GetProps](imapiprop-getprops.md) is called.</span></span> <span data-ttu-id="50f2f-121">Zwar in der Regel eine Anzeige-Tabelle-Benachrichtigung nicht zum Deaktivieren oder Aktivieren eines Steuerelements, können sie mit einer Schaltfläche verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="50f2f-121">Although typically a display table notification cannot be used to disable or enable a control, it can be used with a button.</span></span> <span data-ttu-id="50f2f-122">MAPI wird das geänderte Steuerelement, um auf die Benachrichtigung reagieren aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="50f2f-122">MAPI will refresh the changed control to respond to the notification.</span></span> 
  
<span data-ttu-id="50f2f-123">MAPI-Aufrufen **GetLastError** -Methode des Steuerelements, wenn **Activate** als MAPI_E_USER_CANCEL einen Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50f2f-123">MAPI calls the control's **GetLastError** method when **Activate** returns an error other than MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="50f2f-124">Wenn **GetLastError** erweiterte Fehlerinformationen in der Struktur [MAPIERROR](mapierror.md) , die sie in den Inhalt des Parameters _LppMAPIError_ zurückgibt tätigt, von MAPI für den Benutzer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="50f2f-124">If **GetLastError** places extended error information in the [MAPIERROR](mapierror.md) structure that it returns in the contents of the  _lppMAPIError_ parameter, MAPI displays it for the user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50f2f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50f2f-125">See also</span></span>



[<span data-ttu-id="50f2f-126">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="50f2f-126">MAPI Service Providers</span></span>](mapi-service-providers.md)

