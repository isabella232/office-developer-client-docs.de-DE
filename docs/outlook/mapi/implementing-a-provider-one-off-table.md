---
title: Implementieren einer Anbieter-Einmaltabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 99146f93dcf634be6766f5c6fcc0d1c610b84d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792546"
---
# <a name="implementing-a-provider-one-off-table"></a><span data-ttu-id="b2100-103">Implementieren einer Anbieter-Einmaltabelle</span><span class="sxs-lookup"><span data-stu-id="b2100-103">Implementing a Provider One-Off Table</span></span>

  
  
<span data-ttu-id="b2100-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2100-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2100-105">MAPI-Aufrufen des Anbieters [GetOneOffTable](iablogon-getoneofftable.md) -Methode auf, wenn der Benutzer von einer Clientanwendung eine ausgehende Nachricht einen Empfänger hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b2100-105">MAPI calls your provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method when the user of a client application adds a recipient to an outgoing message.</span></span> <span data-ttu-id="b2100-106">In der Regel sind die angeforderte Adresstypen für Ihr messaging-System eindeutig.</span><span class="sxs-lookup"><span data-stu-id="b2100-106">Typically, the types of addresses requested are unique to your messaging system.</span></span> <span data-ttu-id="b2100-107">Wenn der Anbieter Empfänger erstellen unterstützt, muss sie eine einmalige Tabelle bereitstellen, die Vorlagen für jede Art von unterstützten Empfängeradresse verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="b2100-107">If your provider supports recipient creation, it must supply a one-off table that exposes templates for every type of supported recipient address.</span></span> <span data-ttu-id="b2100-108">Wird vom Dienstanbieter Recipient Creation nicht unterstützt, muss zurückgegeben Sie MAPI_E_NO_SUPPORT aus den Anruf **GetOneOffTable** .</span><span class="sxs-lookup"><span data-stu-id="b2100-108">If your provider does not support recipient creation, return MAPI_E_NO_SUPPORT from the **GetOneOffTable** call.</span></span> 
  
<span data-ttu-id="b2100-109">MAPI wird in der Regel geöffnetem einmaligen Tabelle des Anbieters für die Lebensdauer der Sitzung freigegeben wurde, nur, wenn ein Client des Subsystems aufruft oder Adresse des Buchs [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b2100-109">MAPI will typically keep your provider's one-off table open for the lifetime of the session, releasing it only when a client calls either the subsystem's or address book's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="b2100-110">MAPI registriert für Benachrichtigungen in dieser Tabelle, sodass Vorlagen hinzugefügt oder gelöscht werden, diese Änderungen an den Benutzer widergespiegelt werden können.</span><span class="sxs-lookup"><span data-stu-id="b2100-110">MAPI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span></span> 
  
 <span data-ttu-id="b2100-111">**GetOneOffTable implementieren**</span><span class="sxs-lookup"><span data-stu-id="b2100-111">**To implement IABLogon::GetOneOffTable**</span></span>
  
1. <span data-ttu-id="b2100-112">Überprüfen Sie den Wert des Flags-Parameters, _UlFlags_.</span><span class="sxs-lookup"><span data-stu-id="b2100-112">Check the value of the flags parameter,  _ulFlags_.</span></span> <span data-ttu-id="b2100-113">Wenn die Option MAPI_UNICODE festgelegt ist und der Anbieter keine Unicode unterstützt, ein Fehler auftritt, und geben Sie MAPI_E_BAD_CHARWIDTH zurück.</span><span class="sxs-lookup"><span data-stu-id="b2100-113">If the MAPI_UNICODE flag is set and your provider does not support Unicode, fail and return MAPI_E_BAD_CHARWIDTH.</span></span> 
    
2. <span data-ttu-id="b2100-114">Überprüfen Sie, ob vom Dienstanbieter einmaligen Tabelle bereits erstellt worden ist.</span><span class="sxs-lookup"><span data-stu-id="b2100-114">Check if your provider's one-off table has already been created.</span></span> <span data-ttu-id="b2100-115">Da einmalige Tabellen in der Regel statisch sind, muss der Anbieter nie durch den Erstellungsvorgang nur einmal.</span><span class="sxs-lookup"><span data-stu-id="b2100-115">Because one-off tables are typically static, your provider never has to go through the creation process more than once.</span></span> <span data-ttu-id="b2100-116">Wenn bereits eine Tabelle vorhanden ist, wird zurückkehren Sie einen Zeiger zu ihm.</span><span class="sxs-lookup"><span data-stu-id="b2100-116">If a table already exists, return a pointer to it.</span></span> 
    
3. <span data-ttu-id="b2100-117">Wenn eine einmalige Tabelle noch nicht vorhanden ist, rufen Sie **CreateTable** um eine zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b2100-117">If a one-off table does not yet exist, call **CreateTable** to create one.</span></span> 
    
4. <span data-ttu-id="b2100-118">Legen Sie die folgenden Eigenschaften für die Spalten in der Tabellenzeilen:</span><span class="sxs-lookup"><span data-stu-id="b2100-118">Set the following properties for the columns in your table rows:</span></span>
    
  - <span data-ttu-id="b2100-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) auf den Namen des Typs des Empfängers, die die Vorlage erstellen können.</span><span class="sxs-lookup"><span data-stu-id="b2100-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to the name of the type of recipient that the template can create.</span></span> 
    
  - <span data-ttu-id="b2100-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) an die Eintrags-ID für die einmaligen Vorlage.</span><span class="sxs-lookup"><span data-stu-id="b2100-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) to the entry identifier for the one-off template.</span></span>
    
  - <span data-ttu-id="b2100-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) an, dass der Hierarchieebene in der einmaligen Tabelle werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b2100-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) to indicate the hierarchy level in the one-off table display.</span></span>
    
  - <span data-ttu-id="b2100-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) auf "true", um anzugeben, ob die Zeile einer Vorlage und FALSE darstellt.</span><span class="sxs-lookup"><span data-stu-id="b2100-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) to TRUE to indicate if the row represents a template and FALSE otherwise.</span></span>
    
  - <span data-ttu-id="b2100-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)), die der Art der Adresse, die von der Vorlage erstellt.</span><span class="sxs-lookup"><span data-stu-id="b2100-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the type of address created by the template.</span></span>
    
  - <span data-ttu-id="b2100-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) DT_MAILUSER oder einen anderen Wert, der die Art der Anzeige für die Vorlage angibt.</span><span class="sxs-lookup"><span data-stu-id="b2100-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or another value that indicates the type of display for the template.</span></span>
    
  - <span data-ttu-id="b2100-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) in einen eindeutigen Binärwert.</span><span class="sxs-lookup"><span data-stu-id="b2100-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) to a unique binary value.</span></span> 
    
5. <span data-ttu-id="b2100-126">Rufen Sie [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) , um die Tabelle direkt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b2100-126">Call [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) to modify the table directly.</span></span> 
    
6. <span data-ttu-id="b2100-127">Rufen Sie [ITableData::HrGetView](itabledata-hrgetview.md) So erstellen Sie eine **IMAPITable** Implementierung der Aufrufer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b2100-127">Call [ITableData::HrGetView](itabledata-hrgetview.md) to create an **IMAPITable** interface implementation to return to the caller.</span></span> 
    

