---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Gibt den Typ der verschlüsselten Verbindung an, die für ein SMTP-Konto verwendet werden soll.
ms.openlocfilehash: 67eae5c9c5ca1b7f664ceaac0463ef3f3c9a291a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421284"
---
# <a name="prop_smtp_secure_connection"></a><span data-ttu-id="f15be-103">PROP_SMTP_SECURE_CONNECTION</span><span class="sxs-lookup"><span data-stu-id="f15be-103">PROP_SMTP_SECURE_CONNECTION</span></span>

<span data-ttu-id="f15be-104">Gibt den Typ der verschlüsselten Verbindung an, die für ein SMTP-Konto verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f15be-104">Specifies the type of encrypted connection to use for an SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f15be-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="f15be-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f15be-106">Kennung:</span><span class="sxs-lookup"><span data-stu-id="f15be-106">Identifier:</span></span>  <br/> |<span data-ttu-id="f15be-107">0x020A</span><span class="sxs-lookup"><span data-stu-id="f15be-107">0x020A</span></span>  <br/> |
|<span data-ttu-id="f15be-108">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="f15be-108">Property type:</span></span>  <br/> |<span data-ttu-id="f15be-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="f15be-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="f15be-110">Eigenschaftstag:</span><span class="sxs-lookup"><span data-stu-id="f15be-110">Property tag:</span></span>  <br/> |<span data-ttu-id="f15be-111">0x020A0003</span><span class="sxs-lookup"><span data-stu-id="f15be-111">0x020A0003</span></span>  <br/> |
|<span data-ttu-id="f15be-112">Zugriff:</span><span class="sxs-lookup"><span data-stu-id="f15be-112">Access:</span></span>  <br/> |<span data-ttu-id="f15be-113">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f15be-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f15be-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f15be-114">Remarks</span></span>

<span data-ttu-id="f15be-115">Der Wert kann eine der folgenden Konstanten sein.</span><span class="sxs-lookup"><span data-stu-id="f15be-115">The value can be one of the following constants.</span></span> <span data-ttu-id="f15be-116">Ihre Werte finden Sie unter [Konstanten (Kontoverwaltungs-API).](constants-account-management-api.md)</span><span class="sxs-lookup"><span data-stu-id="f15be-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
|<span data-ttu-id="f15be-117">**Constants**</span><span class="sxs-lookup"><span data-stu-id="f15be-117">**Constants**</span></span>|<span data-ttu-id="f15be-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f15be-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f15be-119">**ENCRYPT_CONN_NO_SECURITY**</span><span class="sxs-lookup"><span data-stu-id="f15be-119">**ENCRYPT_CONN_NO_SECURITY**</span></span> <br/> |<span data-ttu-id="f15be-120">Verwenden Sie keine Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="f15be-120">Do not use any encryption.</span></span>  <br/> |
|<span data-ttu-id="f15be-121">**ENCRYPT_CONN_SSL**</span><span class="sxs-lookup"><span data-stu-id="f15be-121">**ENCRYPT_CONN_SSL**</span></span> <br/> |<span data-ttu-id="f15be-122">Verwenden Sie ssl-Verschlüsselung (Secure Socket Layer).</span><span class="sxs-lookup"><span data-stu-id="f15be-122">Use Secure Socket Layer (SSL) encryption.</span></span>  <br/> |
|<span data-ttu-id="f15be-123">**ENCRYPT_CONN_TLS**</span><span class="sxs-lookup"><span data-stu-id="f15be-123">**ENCRYPT_CONN_TLS**</span></span> <br/> |<span data-ttu-id="f15be-124">Verwenden Sie das TLS-Verschlüsselungs- und -Authentifizierungsprotokoll (Transport Layer Security).</span><span class="sxs-lookup"><span data-stu-id="f15be-124">Use Transport Layer Security (TLS) encryption and authentication protocol.</span></span>  <br/> |
|<span data-ttu-id="f15be-125">**ENCRYPT_CONN_AUTO**</span><span class="sxs-lookup"><span data-stu-id="f15be-125">**ENCRYPT_CONN_AUTO**</span></span> <br/> |<span data-ttu-id="f15be-126">Automatische Erkennung und Verwendung der vom E-Mail-Server unterstützten Verschlüsselungsmethode.</span><span class="sxs-lookup"><span data-stu-id="f15be-126">Automatically detect and use the encryption method supported by the mail server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f15be-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f15be-127">See also</span></span>

- [<span data-ttu-id="f15be-128">Verwalten des Nachrichtendownloads für POP3-Konten</span><span class="sxs-lookup"><span data-stu-id="f15be-128">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="f15be-129">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="f15be-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

