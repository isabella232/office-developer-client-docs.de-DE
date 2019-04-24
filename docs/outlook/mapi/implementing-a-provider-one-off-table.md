---
title: Implementieren einer einmaligen Anbieter Tabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 023686702b76b5b29acf4304fcfdb3377e8cfcff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332865"
---
# <a name="implementing-a-provider-one-off-table"></a><span data-ttu-id="c1f00-103">Implementieren einer einmaligen Anbieter Tabelle</span><span class="sxs-lookup"><span data-stu-id="c1f00-103">Implementing a Provider One-Off Table</span></span>

  
  
<span data-ttu-id="c1f00-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1f00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1f00-105">MAPI Ruft die [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) -Methode Ihres Anbieters auf, wenn der Benutzer einer Clientanwendung einer ausgehenden Nachricht einen Empfänger hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="c1f00-105">MAPI calls your provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method when the user of a client application adds a recipient to an outgoing message.</span></span> <span data-ttu-id="c1f00-106">In der Regel sind die angeforderten Adresstypen für Ihr Messagingsystem eindeutig.</span><span class="sxs-lookup"><span data-stu-id="c1f00-106">Typically, the types of addresses requested are unique to your messaging system.</span></span> <span data-ttu-id="c1f00-107">Wenn Ihr Anbieter die Empfänger Erstellung unterstützt, muss er eine einmalige Tabelle bereitstellen, die Vorlagen für alle unterstützten Empfängeradressen verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="c1f00-107">If your provider supports recipient creation, it must supply a one-off table that exposes templates for every type of supported recipient address.</span></span> <span data-ttu-id="c1f00-108">Wenn Ihr Anbieter die Empfänger Erstellung nicht unterstützt, geben Sie MAPI_E_NO_SUPPORT aus dem **GetOneOffTable** -Aufruf zurück.</span><span class="sxs-lookup"><span data-stu-id="c1f00-108">If your provider does not support recipient creation, return MAPI_E_NO_SUPPORT from the **GetOneOffTable** call.</span></span> 
  
<span data-ttu-id="c1f00-109">In der Regel wird die einmalige Tabelle Ihres Anbieters für die gesamte Lebensdauer der Sitzung geöffnet, und Sie wird nur dann freigegeben, wenn ein Client die [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode des Subsystems oder des Adressbuchs aufruft.</span><span class="sxs-lookup"><span data-stu-id="c1f00-109">MAPI will typically keep your provider's one-off table open for the lifetime of the session, releasing it only when a client calls either the subsystem's or address book's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="c1f00-110">MAPI registriert für Benachrichtigungen in dieser Tabelle, sodass diese Änderungen für den Benutzer reflektiert werden können, wenn Vorlagen hinzugefügt oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="c1f00-110">MAPI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span></span> 
  
 <span data-ttu-id="c1f00-111">**So implementieren Sie IABLogon:: GetOneOffTable**</span><span class="sxs-lookup"><span data-stu-id="c1f00-111">**To implement IABLogon::GetOneOffTable**</span></span>
  
1. <span data-ttu-id="c1f00-112">Überprüfen Sie den Wert des flags-Parameters _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="c1f00-112">Check the value of the flags parameter,  _ulFlags_.</span></span> <span data-ttu-id="c1f00-113">Wenn das MAPI_UNICODE-Flag festgelegt ist und Ihr Anbieter Unicode nicht unterstützt, schlagen Sie fehl und geben MAPI_E_BAD_CHARWIDTH zurück.</span><span class="sxs-lookup"><span data-stu-id="c1f00-113">If the MAPI_UNICODE flag is set and your provider does not support Unicode, fail and return MAPI_E_BAD_CHARWIDTH.</span></span> 
    
2. <span data-ttu-id="c1f00-114">Überprüfen Sie, ob die einmalige Tabelle Ihres Anbieters bereits erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c1f00-114">Check if your provider's one-off table has already been created.</span></span> <span data-ttu-id="c1f00-115">Da einmalige Tabellen in der Regel statisch sind, muss Ihr Anbieter den Erstellungsprozess nie mehr als einmal durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="c1f00-115">Because one-off tables are typically static, your provider never has to go through the creation process more than once.</span></span> <span data-ttu-id="c1f00-116">Wenn bereits eine Tabelle vorhanden ist, geben Sie einen Zeiger darauf zurück.</span><span class="sxs-lookup"><span data-stu-id="c1f00-116">If a table already exists, return a pointer to it.</span></span> 
    
3. <span data-ttu-id="c1f00-117">Wenn noch keine einmalige Tabelle vorhanden ist, rufen Sie **Create** Table auf, um eine zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c1f00-117">If a one-off table does not yet exist, call **CreateTable** to create one.</span></span> 
    
4. <span data-ttu-id="c1f00-118">Legen Sie die folgenden Eigenschaften für die Spalten in den Tabellenzeilen fest:</span><span class="sxs-lookup"><span data-stu-id="c1f00-118">Set the following properties for the columns in your table rows:</span></span>
    
  - <span data-ttu-id="c1f00-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) an den Namen des Empfängertyps, der von der Vorlage erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c1f00-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to the name of the type of recipient that the template can create.</span></span> 
    
  - <span data-ttu-id="c1f00-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) an die Eintrags-ID für die einmalige Vorlage.</span><span class="sxs-lookup"><span data-stu-id="c1f00-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) to the entry identifier for the one-off template.</span></span>
    
  - <span data-ttu-id="c1f00-121">**PR_DEPTH** ([Pidtagdepth (](pidtagdepth-canonical-property.md)), um die Hierarchieebene in der einmaligen Tabellenanzeige anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c1f00-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) to indicate the hierarchy level in the one-off table display.</span></span>
    
  - <span data-ttu-id="c1f00-122">**PR_SELECTABLE** ([Pidtagselectable (](pidtagselectable-canonical-property.md)) auf true, um anzugeben, ob die Zeile eine Vorlage darstellt, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="c1f00-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) to TRUE to indicate if the row represents a template and FALSE otherwise.</span></span>
    
  - <span data-ttu-id="c1f00-123">**PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md)) an den Typ der von der Vorlage erstellten Adresse.</span><span class="sxs-lookup"><span data-stu-id="c1f00-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the type of address created by the template.</span></span>
    
  - <span data-ttu-id="c1f00-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) an DT_MAILUSER oder einen anderen Wert, der den Anzeigetyp für die Vorlage angibt.</span><span class="sxs-lookup"><span data-stu-id="c1f00-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or another value that indicates the type of display for the template.</span></span>
    
  - <span data-ttu-id="c1f00-125">**PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md)) an einen eindeutigen Binärwert.</span><span class="sxs-lookup"><span data-stu-id="c1f00-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) to a unique binary value.</span></span> 
    
5. <span data-ttu-id="c1f00-126">Rufen Sie [ITableData:: HrModifyRow](itabledata-hrmodifyrow.md) auf, um die Tabelle direkt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c1f00-126">Call [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) to modify the table directly.</span></span> 
    
6. <span data-ttu-id="c1f00-127">Rufen Sie [ITableData:: HrGetView](itabledata-hrgetview.md) auf, um eine **IMAPITable** -Schnittstellenimplementierung zum zurückkehren zum Aufrufer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c1f00-127">Call [ITableData::HrGetView](itabledata-hrgetview.md) to create an **IMAPITable** interface implementation to return to the caller.</span></span> 
    

