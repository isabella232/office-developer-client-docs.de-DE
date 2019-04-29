---
title: Informationen zur Kontoverwaltungs-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'Die Account Management-API bietet Zugriff auf Kontoinformationen und unterstützt Benachrichtigungen über Kontoänderungen. Als Clients dieser API führen e-Mail-Anbieter folgende Aktionen aus:'
ms.openlocfilehash: 76520b7cc7f28ede28257729e4e4fbe2d5096290
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426249"
---
# <a name="about-the-account-management-api"></a><span data-ttu-id="2bc81-104">Informationen zur Kontoverwaltungs-API</span><span class="sxs-lookup"><span data-stu-id="2bc81-104">About the Account Management API</span></span>

<span data-ttu-id="2bc81-105">Die Account Management-API bietet Zugriff auf Kontoinformationen und unterstützt Benachrichtigungen über Kontoänderungen.</span><span class="sxs-lookup"><span data-stu-id="2bc81-105">The Account Management API provides access to account information and supports notifications of account changes.</span></span> <span data-ttu-id="2bc81-106">Als Clients dieser API führen e-Mail-Anbieter folgende Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="2bc81-106">As clients of this API, mail providers do the following:</span></span>
  
1. <span data-ttu-id="2bc81-107">Verwenden Sie [IOlkAccountManager](iolkaccountmanager.md) , um den Zugriff auf Konten zu verwalten und Benachrichtigungen zu Kontoänderungen einzurichten.</span><span class="sxs-lookup"><span data-stu-id="2bc81-107">Use [IOlkAccountManager](iolkaccountmanager.md) to manage access to accounts and set up notifications about account changes.</span></span> 
    
2. <span data-ttu-id="2bc81-108">Implementieren und Verwenden von [IOlkAccountNotify](iolkaccountnotify.md) zum Senden von Benachrichtigungen zu Kontoänderungen.</span><span class="sxs-lookup"><span data-stu-id="2bc81-108">Implement and use [IOlkAccountNotify](iolkaccountnotify.md) to send notifications about account changes.</span></span> 
    
3. <span data-ttu-id="2bc81-109">Verwenden Sie [IOlkEnum](iolkenum.md) zum Aufzählen von Konten.</span><span class="sxs-lookup"><span data-stu-id="2bc81-109">Use [IOlkEnum](iolkenum.md) to enumerate accounts.</span></span> 
    
4. <span data-ttu-id="2bc81-110">Verwenden Sie [IOlkAccount](iolkaccount.md) , um Eigenschaften und andere Informationen zu einem Konto abzurufen und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2bc81-110">Use [IOlkAccount](iolkaccount.md) to get and set properties and other information about an account.</span></span> <span data-ttu-id="2bc81-111">Clients rufen diese Schnittstelle über [IOlkAccountManager:: FindAccount](iolkaccountmanager-findaccount.md) oder [IOlkEnum:: GetNext](iolkenum-getnext.md) ab, um auf ein einzelnes Konto zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="2bc81-111">Clients obtain this interface through [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) or [IOlkEnum::GetNext](iolkenum-getnext.md) to access an individual account.</span></span> 
    
5. <span data-ttu-id="2bc81-112">Implementieren und verwenden Sie [IOlkAccountHelper](iolkaccounthelper.md) , um die Hilfsfunktion des Konto-Managers bereitzustellen, einschließlich dem Profilnamen eines Kontos und der aktuellen MAPI-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="2bc81-112">Implement and use [IOlkAccountHelper](iolkaccounthelper.md) to provide the account manager helper functionality, including getting an account's profile name and the current MAPI session.</span></span> 
    
6. <span data-ttu-id="2bc81-113">Implementieren und verwenden Sie [IOlkErrorUnknown](iolkerrorunknown.md) , um zusätzliche Informationen zu einem Fehler in **IOlkAccountManager**, **IOlkAccountNotify**und **IOlkAccount**bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2bc81-113">Implement and use [IOlkErrorUnknown](iolkerrorunknown.md) to provide extra information about an error in **IOlkAccountManager**, **IOlkAccountNotify**, and **IOlkAccount**.</span></span> 

##  <a name="account-management-api-components"></a><span data-ttu-id="2bc81-114">API-Komponenten für die Kontoverwaltung</span><span class="sxs-lookup"><span data-stu-id="2bc81-114">Account Management API components</span></span>

<span data-ttu-id="2bc81-115">Die Account Management-API bietet die folgenden Definitionen, Datentypen, Schnittstellen, benannten Eigenschaften und Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2bc81-115">The Account Management API provides the following definitions, data types, interfaces, named properties, and properties.</span></span>
  
### <a name="definitions"></a><span data-ttu-id="2bc81-116">Definitionen</span><span class="sxs-lookup"><span data-stu-id="2bc81-116">Definitions</span></span>
  
- [<span data-ttu-id="2bc81-117">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="2bc81-117">Constants (Account management API)</span></span>](constants-account-management-api.md)
    
### <a name="data-types"></a><span data-ttu-id="2bc81-118">Datentypen</span><span class="sxs-lookup"><span data-stu-id="2bc81-118">Data types</span></span>
  
- [<span data-ttu-id="2bc81-119">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="2bc81-119">ACCT_BIN</span></span>](acct_bin.md)
    
- [<span data-ttu-id="2bc81-120">ACCT_VARIANT</span><span class="sxs-lookup"><span data-stu-id="2bc81-120">ACCT_VARIANT</span></span>](acct_variant.md)
    
### <a name="interfaces"></a><span data-ttu-id="2bc81-121">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2bc81-121">Interfaces</span></span>
  
- [<span data-ttu-id="2bc81-122">IOlkAccount</span><span class="sxs-lookup"><span data-stu-id="2bc81-122">IOlkAccount</span></span>](iolkaccount.md)
    
- [<span data-ttu-id="2bc81-123">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="2bc81-123">IOlkAccountHelper</span></span>](iolkaccounthelper.md)
    
- [<span data-ttu-id="2bc81-124">IOlkAccountManager</span><span class="sxs-lookup"><span data-stu-id="2bc81-124">IOlkAccountManager</span></span>](iolkaccountmanager.md)
    
- [<span data-ttu-id="2bc81-125">IOlkAccountNotify</span><span class="sxs-lookup"><span data-stu-id="2bc81-125">IOlkAccountNotify</span></span>](iolkaccountnotify.md)
    
- [<span data-ttu-id="2bc81-126">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="2bc81-126">IOlkEnum</span></span>](iolkenum.md)
    
- [<span data-ttu-id="2bc81-127">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="2bc81-127">IOlkErrorUnknown</span></span>](iolkerrorunknown.md)
    
### <a name="named-properties"></a><span data-ttu-id="2bc81-128">Benannte Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2bc81-128">Named properties</span></span>
  
- [<span data-ttu-id="2bc81-129">PidLidInternetAccountName</span><span class="sxs-lookup"><span data-stu-id="2bc81-129">PidLidInternetAccountName</span></span>](pidlidinternetaccountname.md)
    
- [<span data-ttu-id="2bc81-130">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="2bc81-130">PidLidInternetAccountStamp</span></span>](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a><span data-ttu-id="2bc81-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2bc81-131">Properties</span></span>
  
- [<span data-ttu-id="2bc81-132">PidTagNextSendAcct</span><span class="sxs-lookup"><span data-stu-id="2bc81-132">PidTagNextSendAcct</span></span>](pidtagnextsendacct.md)
    
- [<span data-ttu-id="2bc81-133">PidTagPrimarySendAccount</span><span class="sxs-lookup"><span data-stu-id="2bc81-133">PidTagPrimarySendAccount</span></span>](pidtagprimarysendaccount.md)
    
- [<span data-ttu-id="2bc81-134">PROP_ACCT_DELIVERY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="2bc81-134">PROP_ACCT_DELIVERY_FOLDER</span></span>](prop_acct_delivery_folder.md)
    
- [<span data-ttu-id="2bc81-135">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="2bc81-135">PROP_ACCT_DELIVERY_STORE</span></span>](prop_acct_delivery_store.md)
    
- [<span data-ttu-id="2bc81-136">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="2bc81-136">PROP_ACCT_ID</span></span>](prop_acct_id.md)
    
- [<span data-ttu-id="2bc81-137">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="2bc81-137">PROP_ACCT_IS_EXCH</span></span>](prop_acct_is_exch.md)
    
- [<span data-ttu-id="2bc81-138">PROP_ACCT_NAME</span><span class="sxs-lookup"><span data-stu-id="2bc81-138">PROP_ACCT_NAME</span></span>](prop_acct_name.md)
    
- [<span data-ttu-id="2bc81-139">PROP_ACCT_PREFERENCES_UID</span><span class="sxs-lookup"><span data-stu-id="2bc81-139">PROP_ACCT_PREFERENCES_UID</span></span>](prop_acct_preferences_uid.md)
    
- [<span data-ttu-id="2bc81-140">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="2bc81-140">PROP_ACCT_SEND_STAMP</span></span>](prop_acct_send_stamp.md)
    
- [<span data-ttu-id="2bc81-141">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="2bc81-141">PROP_ACCT_SENTITEMS_EID</span></span>](prop_acct_sentitems_eid.md)
    
- [<span data-ttu-id="2bc81-142">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="2bc81-142">PROP_ACCT_STAMP</span></span>](prop_acct_stamp.md)
    
- [<span data-ttu-id="2bc81-143">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="2bc81-143">PROP_ACCT_USER_EMAIL_ADDR</span></span>](prop_acct_user_email_addr.md)
    
- [<span data-ttu-id="2bc81-144">PROP_ACCT_USER_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="2bc81-144">PROP_ACCT_USER_DISPLAY_NAME</span></span>](prop_acct_user_display_name.md)
    
- [<span data-ttu-id="2bc81-145">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="2bc81-145">PROP_MAPI_EMSMDB_UID</span></span>](prop_mapi_emsmdb_uid.md)
    
- [<span data-ttu-id="2bc81-146">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2bc81-146">PROP_MAPI_IDENTITY_ENTRYID</span></span>](prop_mapi_identity_entryid.md)
    
- [<span data-ttu-id="2bc81-147">PROP_MAPI_TRANSPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="2bc81-147">PROP_MAPI_TRANSPORT_FLAGS</span></span>](prop_mapi_transport_flags.md)
    

