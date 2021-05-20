---
title: Implementieren eines Anbieters One-Off Tabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 023686702b76b5b29acf4304fcfdb3377e8cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436293"
---
# <a name="implementing-a-provider-one-off-table"></a><span data-ttu-id="78749-103">Implementieren eines Anbieters One-Off Tabelle</span><span class="sxs-lookup"><span data-stu-id="78749-103">Implementing a Provider One-Off Table</span></span>

  
  
<span data-ttu-id="78749-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78749-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78749-105">MAPI ruft die [IABLogon::GetOneOffTable-Methode](iablogon-getoneofftable.md) Ihres Anbieters auf, wenn der Benutzer einer Clientanwendung einer ausgehenden Nachricht einen Empfänger hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="78749-105">MAPI calls your provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method when the user of a client application adds a recipient to an outgoing message.</span></span> <span data-ttu-id="78749-106">In der Regel sind die angeforderten Adresstypen für Ihr Messagingsystem eindeutig.</span><span class="sxs-lookup"><span data-stu-id="78749-106">Typically, the types of addresses requested are unique to your messaging system.</span></span> <span data-ttu-id="78749-107">Wenn Ihr Anbieter die Erstellung von Empfängern unterstützt, muss er eine einzelne Tabelle angeben, in der Vorlagen für jeden Typ unterstützter Empfängeradressen verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="78749-107">If your provider supports recipient creation, it must supply a one-off table that exposes templates for every type of supported recipient address.</span></span> <span data-ttu-id="78749-108">Wenn Ihr Anbieter die Erstellung von Empfängern nicht unterstützt, geben MAPI_E_NO_SUPPORT vom **GetOneOffTable-Aufruf** zurück.</span><span class="sxs-lookup"><span data-stu-id="78749-108">If your provider does not support recipient creation, return MAPI_E_NO_SUPPORT from the **GetOneOffTable** call.</span></span> 
  
<span data-ttu-id="78749-109">MAPI hält in der Regel die einmal geöffnete Tabelle Ihres Anbieters für die Lebensdauer der Sitzung offen und gibt sie nur frei, wenn ein Client die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) des Subsystems oder adressbuchs aufruft.</span><span class="sxs-lookup"><span data-stu-id="78749-109">MAPI will typically keep your provider's one-off table open for the lifetime of the session, releasing it only when a client calls either the subsystem's or address book's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="78749-110">MAPI registriert sich für Benachrichtigungen in dieser Tabelle, sodass beim Hinzufügen oder Löschen von Vorlagen diese Änderungen für den Benutzer widerspiegelt werden können.</span><span class="sxs-lookup"><span data-stu-id="78749-110">MAPI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span></span> 
  
 <span data-ttu-id="78749-111">**So implementieren Sie IABLogon::GetOneOffTable**</span><span class="sxs-lookup"><span data-stu-id="78749-111">**To implement IABLogon::GetOneOffTable**</span></span>
  
1. <span data-ttu-id="78749-112">Überprüfen Sie den Wert des Flags-Parameters  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="78749-112">Check the value of the flags parameter,  _ulFlags_.</span></span> <span data-ttu-id="78749-113">Wenn das MAPI_UNICODE festgelegt ist und Ihr Anbieter Unicode nicht unterstützt, führen Sie einen Fehler aus, und geben Sie MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="78749-113">If the MAPI_UNICODE flag is set and your provider does not support Unicode, fail and return MAPI_E_BAD_CHARWIDTH.</span></span> 
    
2. <span data-ttu-id="78749-114">Überprüfen Sie, ob die einmal erstellte Tabelle Ihres Anbieters bereits erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="78749-114">Check if your provider's one-off table has already been created.</span></span> <span data-ttu-id="78749-115">Da die Tabellen in der Regel statisch sind, muss Ihr Anbieter den Erstellungsprozess niemals mehr als einmal durchgehen.</span><span class="sxs-lookup"><span data-stu-id="78749-115">Because one-off tables are typically static, your provider never has to go through the creation process more than once.</span></span> <span data-ttu-id="78749-116">Wenn bereits eine Tabelle vorhanden ist, geben Sie einen Zeiger auf sie zurück.</span><span class="sxs-lookup"><span data-stu-id="78749-116">If a table already exists, return a pointer to it.</span></span> 
    
3. <span data-ttu-id="78749-117">Wenn noch keine einzige Tabelle vorhanden ist, rufen Sie **CreateTable auf,** um eine zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="78749-117">If a one-off table does not yet exist, call **CreateTable** to create one.</span></span> 
    
4. <span data-ttu-id="78749-118">Legen Sie die folgenden Eigenschaften für die Spalten in den Tabellenzeilen ein:</span><span class="sxs-lookup"><span data-stu-id="78749-118">Set the following properties for the columns in your table rows:</span></span>
    
  - <span data-ttu-id="78749-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) auf den Namen des Empfängertyps, den die Vorlage erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="78749-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to the name of the type of recipient that the template can create.</span></span> 
    
  - <span data-ttu-id="78749-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) zur Eintrags-ID für die einmal vorlage.</span><span class="sxs-lookup"><span data-stu-id="78749-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) to the entry identifier for the one-off template.</span></span>
    
  - <span data-ttu-id="78749-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) zum Angeben der Hierarchieebene in der Tabellenanzeige.</span><span class="sxs-lookup"><span data-stu-id="78749-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) to indicate the hierarchy level in the one-off table display.</span></span>
    
  - <span data-ttu-id="78749-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) auf TRUE, um anzugeben, ob die Zeile eine Vorlage und andernfalls FALSE darstellt.</span><span class="sxs-lookup"><span data-stu-id="78749-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) to TRUE to indicate if the row represents a template and FALSE otherwise.</span></span>
    
  - <span data-ttu-id="78749-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) auf den Von der Vorlage erstellten Adresstyp an.</span><span class="sxs-lookup"><span data-stu-id="78749-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the type of address created by the template.</span></span>
    
  - <span data-ttu-id="78749-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) auf DT_MAILUSER oder einen anderen Wert, der den Anzeigetyp für die Vorlage angibt.</span><span class="sxs-lookup"><span data-stu-id="78749-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or another value that indicates the type of display for the template.</span></span>
    
  - <span data-ttu-id="78749-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) auf einen eindeutigen binären Wert.</span><span class="sxs-lookup"><span data-stu-id="78749-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) to a unique binary value.</span></span> 
    
5. <span data-ttu-id="78749-126">Rufen [Sie ITableData::HrModifyRow auf,](itabledata-hrmodifyrow.md) um die Tabelle direkt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="78749-126">Call [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) to modify the table directly.</span></span> 
    
6. <span data-ttu-id="78749-127">Rufen [Sie ITableData::HrGetView auf,](itabledata-hrgetview.md) um eine **IMAPITable-Schnittstellenimplementierung** zu erstellen, um zum Aufrufer zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="78749-127">Call [ITableData::HrGetView](itabledata-hrgetview.md) to create an **IMAPITable** interface implementation to return to the caller.</span></span> 
    

