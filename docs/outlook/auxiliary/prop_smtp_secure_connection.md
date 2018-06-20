---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Gibt den Typ des verschlüsselten Verbindungstyp für SMTP-Konto verwenden.
ms.openlocfilehash: e1c8c8dacf953407d4cbb114aa5ee0a4cdb6acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791202"
---
# <a name="propsmtpsecureconnection"></a><span data-ttu-id="79b0f-103">PROP_SMTP_SECURE_CONNECTION</span><span class="sxs-lookup"><span data-stu-id="79b0f-103">PROP_SMTP_SECURE_CONNECTION</span></span>

<span data-ttu-id="79b0f-104">Gibt den Typ des verschlüsselten Verbindungstyp für SMTP-Konto verwenden.</span><span class="sxs-lookup"><span data-stu-id="79b0f-104">Specifies the type of encrypted connection to use for an SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="79b0f-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="79b0f-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79b0f-106">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="79b0f-106">Identifier:</span></span>  <br/> |<span data-ttu-id="79b0f-107">0x020A</span><span class="sxs-lookup"><span data-stu-id="79b0f-107">0x020A</span></span>  <br/> |
|<span data-ttu-id="79b0f-108">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="79b0f-108">Property type:</span></span>  <br/> |<span data-ttu-id="79b0f-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="79b0f-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="79b0f-110">Eigenschafts-Tag:</span><span class="sxs-lookup"><span data-stu-id="79b0f-110">Property tag:</span></span>  <br/> |<span data-ttu-id="79b0f-111">0x020A0003</span><span class="sxs-lookup"><span data-stu-id="79b0f-111">0x020A0003</span></span>  <br/> |
|<span data-ttu-id="79b0f-112">Access:</span><span class="sxs-lookup"><span data-stu-id="79b0f-112">Access:</span></span>  <br/> |<span data-ttu-id="79b0f-113">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="79b0f-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79b0f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="79b0f-114">Remarks</span></span>

<span data-ttu-id="79b0f-115">Der Wert kann eine der folgenden Konstanten sein.</span><span class="sxs-lookup"><span data-stu-id="79b0f-115">The value can be one of the following constants.</span></span> <span data-ttu-id="79b0f-116">Ihren Werten finden Sie unter [Konstanten (Konto Management-API)](constants-account-management-api.md) .</span><span class="sxs-lookup"><span data-stu-id="79b0f-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
|<span data-ttu-id="79b0f-117">**Konstanten**</span><span class="sxs-lookup"><span data-stu-id="79b0f-117">**Constants**</span></span>|<span data-ttu-id="79b0f-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="79b0f-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="79b0f-119">**ENCRYPT_CONN_NO_SECURITY**</span><span class="sxs-lookup"><span data-stu-id="79b0f-119">**ENCRYPT_CONN_NO_SECURITY**</span></span> <br/> |<span data-ttu-id="79b0f-120">Verwenden Sie keine Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="79b0f-120">Do not use any encryption.</span></span>  <br/> |
|<span data-ttu-id="79b0f-121">**ENCRYPT_CONN_SSL**</span><span class="sxs-lookup"><span data-stu-id="79b0f-121">**ENCRYPT_CONN_SSL**</span></span> <br/> |<span data-ttu-id="79b0f-122">Verschlüsselung Secure Socket Layer (SSL) verwenden.</span><span class="sxs-lookup"><span data-stu-id="79b0f-122">Use Secure Socket Layer (SSL) encryption.</span></span>  <br/> |
|<span data-ttu-id="79b0f-123">**ENCRYPT_CONN_TLS**</span><span class="sxs-lookup"><span data-stu-id="79b0f-123">**ENCRYPT_CONN_TLS**</span></span> <br/> |<span data-ttu-id="79b0f-124">Verschlüsselung und Authentifizierung-Protokoll (Transport Layer Security, TLS) verwenden.</span><span class="sxs-lookup"><span data-stu-id="79b0f-124">Use Transport Layer Security (TLS) encryption and authentication protocol.</span></span>  <br/> |
|<span data-ttu-id="79b0f-125">**ENCRYPT_CONN_AUTO**</span><span class="sxs-lookup"><span data-stu-id="79b0f-125">**ENCRYPT_CONN_AUTO**</span></span> <br/> |<span data-ttu-id="79b0f-126">Automatisch erkennen Sie und die Verschlüsselungsmethode vom Mailserver unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79b0f-126">Automatically detect and use the encryption method supported by the mail server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="79b0f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79b0f-127">See also</span></span>

- [<span data-ttu-id="79b0f-128">Verwalten von Nachricht downloads für POP3-Konten</span><span class="sxs-lookup"><span data-stu-id="79b0f-128">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="79b0f-129">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="79b0f-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

