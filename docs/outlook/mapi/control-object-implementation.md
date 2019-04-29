---
title: Implementierung des Control-Objekts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ad62ff0-c527-4e75-a2af-b5906a7588e8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8304021565638f8a5893d0be8cd6a94ed62a8d95
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422607"
---
# <a name="control-object-implementation"></a><span data-ttu-id="51500-103">Implementierung des Control-Objekts</span><span class="sxs-lookup"><span data-stu-id="51500-103">Control Object Implementation</span></span>

  
  
<span data-ttu-id="51500-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51500-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51500-105">Steuerelementobjekte oder Objekte, die die [IMAPIControl: IUnknown](imapicontroliunknown.md) -Schnittstelle unterstützen, werden von Anbietern implementiert, um einer Schaltfläche, die in einem MAPI-Dialogfeld angezeigt wird, Funktionalität hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="51500-105">Control objects, or objects that support the [IMAPIControl : IUnknown](imapicontroliunknown.md) interface, are implemented by providers to add functionality to a button that appears on a MAPI dialog box.</span></span> <span data-ttu-id="51500-106">Steuerelemente können nur für Schaltflächen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="51500-106">Control objects can only be implemented for buttons.</span></span> 
  
 <span data-ttu-id="51500-107">**IMAPIControl** verfügt über drei Methoden: [Getlasterroraufzurufen](imapicontrol-getlasterror.md), GetState und [Activate](imapicontrol-activate.md). [](imapicontrol-getstate.md)</span><span class="sxs-lookup"><span data-stu-id="51500-107">**IMAPIControl** has three methods: [GetLastError](imapicontrol-getlasterror.md), [GetState](imapicontrol-getstate.md), and [Activate](imapicontrol-activate.md).</span></span> 
  
<span data-ttu-id="51500-108">MAPI ruft **GetState** auf, um zu bestimmen, ob die Schaltfläche deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="51500-108">MAPI calls **GetState** to determine whether or not to disable the button.</span></span> <span data-ttu-id="51500-109">**GetState** wird in den folgenden Situationen aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="51500-109">**GetState** is called in the following situations:</span></span> 
  
- <span data-ttu-id="51500-110">Wenn das Dialogfeld, in dem die Schaltfläche angezeigt wird, zuerst angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="51500-110">When the dialog box on which the button appears is first displayed.</span></span>
    
- <span data-ttu-id="51500-111">Wenn eine Anzeige Tabellenbenachrichtigung für die Schaltfläche ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="51500-111">When a display table notification is issued for the button.</span></span> 
    
<span data-ttu-id="51500-112">Legen Sie den Inhalt des _lpulState_ -Parameters auf MAPI_DISABLED fest, wenn der Benutzer nicht mit der Schaltfläche und MAPI_ENABLED interagieren kann, wenn der Benutzer interagieren darf.</span><span class="sxs-lookup"><span data-stu-id="51500-112">Set the contents of the  _lpulState_ parameter to MAPI_DISABLED if the user cannot interact with the button and MAPI_ENABLED if the user can interact.</span></span> 
  
<span data-ttu-id="51500-113">Wenn der Benutzer auf die Schaltfläche klickt, ruft MAPI die **Aktivierung**auf.</span><span class="sxs-lookup"><span data-stu-id="51500-113">When the user clicks the button, MAPI calls **Activate**.</span></span> <span data-ttu-id="51500-114">**Activate** führt die Aufgabe aus, die der Schaltfläche zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="51500-114">**Activate** performs the task that has been associated with the button.</span></span> <span data-ttu-id="51500-115">Diese Aufgabe kann für Ihren Anbieter geeignet sein, wie beispielsweise Anzeigen eines Dialogfelds oder Aktualisieren einer Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="51500-115">This task can be anything appropriate for your provider, such as displaying a dialog box or updating a property.</span></span> <span data-ttu-id="51500-116">Wenn die Aufgabe nicht erfolgreich ist, weil der Benutzer sie abgebrochen hat, geben Sie MAPI_E_USER_CANCEL zurück.</span><span class="sxs-lookup"><span data-stu-id="51500-116">If the task is unsuccessful because the user canceled it, return MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="51500-117">Geben Sie für weitere Fehlerursachen den entsprechenden Fehlerwert zurück.</span><span class="sxs-lookup"><span data-stu-id="51500-117">For other causes of failure, return the appropriate error value.</span></span> 
  
<span data-ttu-id="51500-118">Wenn die Aufgabe erfolgreich ist und mit einer Eigenschaftenänderung verknüpft ist, die in einem anderen Steuerelement des Dialogfelds angezeigt wird, rufen Sie [ITableData:: HrNotify](itabledata-hrnotify.md)auf.</span><span class="sxs-lookup"><span data-stu-id="51500-118">If the task is successful and it is linked to a property change that is reflected in another control on the dialog box, call [ITableData::HrNotify](itabledata-hrnotify.md).</span></span> <span data-ttu-id="51500-119">**HrNotify** wird aufgerufen, um eine Anzeige Tabellenbenachrichtigung mit der **PR_CONTROL_ID** ([pidtagcontrolid (](pidtagcontrolid-canonical-property.md))-Eigenschaft der geänderten Eigenschaft in der [TABLE_NOTIFICATION](table_notification.md) -Struktur auszugeben.</span><span class="sxs-lookup"><span data-stu-id="51500-119">**HrNotify** is called to issue a display table notification with the changed property's **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) property in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> <span data-ttu-id="51500-120">Platzieren Sie den neuen Eigenschaftswert nicht in der Struktur; Geben Sie Sie stattdessen zurück, wenn [IMAPIProp::](imapiprop-getprops.md) GetProps aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="51500-120">Do not place the new property value in the structure; instead, return it when [IMAPIProp::GetProps](imapiprop-getprops.md) is called.</span></span> <span data-ttu-id="51500-121">Zwar kann in der Regel eine Anzeige Tabellenbenachrichtigung nicht zum Deaktivieren oder Aktivieren eines Steuerelements verwendet werden, es kann jedoch mit einer Schaltfläche verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51500-121">Although typically a display table notification cannot be used to disable or enable a control, it can be used with a button.</span></span> <span data-ttu-id="51500-122">MAPI aktualisiert das geänderte Steuerelement so, dass es auf die Benachrichtigung reagiert.</span><span class="sxs-lookup"><span data-stu-id="51500-122">MAPI will refresh the changed control to respond to the notification.</span></span> 
  
<span data-ttu-id="51500-123">MAPI Ruft die **getlasterroraufzurufen** -Methode des Steuerelements auf, wenn **Activate** einen anderen Fehler als MAPI_E_USER_CANCEL zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="51500-123">MAPI calls the control's **GetLastError** method when **Activate** returns an error other than MAPI_E_USER_CANCEL.</span></span> <span data-ttu-id="51500-124">Wenn **getlasterroraufzurufen** in der [MAPIERROR](mapierror.md) -Struktur erweiterte Fehlerinformationen platziert, die im Inhalt des _lppMAPIError_ -Parameters zurückGEGEBEN werden, wird diese von MAPI für den Benutzer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51500-124">If **GetLastError** places extended error information in the [MAPIERROR](mapierror.md) structure that it returns in the contents of the  _lppMAPIError_ parameter, MAPI displays it for the user.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="51500-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51500-125">See also</span></span>



[<span data-ttu-id="51500-126">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="51500-126">MAPI Service Providers</span></span>](mapi-service-providers.md)

