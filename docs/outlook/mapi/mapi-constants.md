---
title: MAPI-Konstanten
manager: soliver
ms.date: 10/02/2018
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8fa5ac8d-3f63-499c-bb4e-439984773e4a
description: Konstantendefinitionen, MAPI-Schnittstellendeklarationen und Klassen- und Schnittstellenbezeichner, die von den MAPI-APIs verwendet werden
ms.openlocfilehash: 343b777550d88276a1f5cad19f12ae7fc09c6244
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318921"
---
# <a name="mapi-constants"></a><span data-ttu-id="12438-103">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="12438-103">MAPI constants</span></span>

<span data-ttu-id="12438-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12438-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12438-105">Dieser Abschnitt enthält die Konstantendefinitionen, MAPI-Schnittstellendeklarationen und Klassen- und Schnittstellenbezeichner, die von den MAPI-APIs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12438-105">This topic contains constant definitions, MAPI interface declarations, and class and interface identifiers used by the MAPI APIs.</span></span>
  
## <a name="class-and-interface-identifiers"></a><span data-ttu-id="12438-106">Klassen- und Schnittstellenbezeichner</span><span class="sxs-lookup"><span data-stu-id="12438-106">Class and interface identifiers</span></span>

<span data-ttu-id="12438-107">Verwenden Sie das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef.h definierte DEFINE_GUID-Makro, um symbolischen GUID-Namen (Globally Unique Identifier) Ihre Werte zuzuordnen (falls nicht anders angegeben).</span><span class="sxs-lookup"><span data-stu-id="12438-107">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values, unless otherwise indicated.</span></span>
  
## <a name="attachment-security-conversion-api"></a><span data-ttu-id="12438-108">Anlagensicherheit-Konvertierungs-API</span><span class="sxs-lookup"><span data-stu-id="12438-108">Attachment security conversion API</span></span>

<span data-ttu-id="12438-109">Dieser Abschnitt enthält Konstantendefinitionen und Schnittstellenbezeichner für die Anlagensicherheit-API.</span><span class="sxs-lookup"><span data-stu-id="12438-109">This section contains constant definitions and interface identifiers for the Attachment Security API.</span></span>
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

<span data-ttu-id="12438-110">Verwenden Sie das in der Windows SDK-Headerdatei mapidefs.h definierte MAPIMETHOD-Makro, um die rein virtuelle Funktion **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)** zu definieren.</span><span class="sxs-lookup"><span data-stu-id="12438-110">Use the MAPIMETHOD macro defined in the Windows SDK header file mapidefs.h to define the pure virtual function **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span></span> 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

<span data-ttu-id="12438-111">Verwenden Sie das in der Windows SDK-Headerdatei mapidefs.h definierte DECLARE_MAPI_INTERFACE_-Makro, um die Tabelle virtueller Methoden für **[IAttachmentSecurity](iattachmentsecurityiunknown.md)** zu definieren.</span><span class="sxs-lookup"><span data-stu-id="12438-111">Use the DECLARE_MAPI_INTERFACE_ macro defined in the Windows SDK header file mapidefs.h to define the virtual method table for **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span></span> 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a><span data-ttu-id="12438-112">MAPI-MIME-Konvertierungs-API</span><span class="sxs-lookup"><span data-stu-id="12438-112">MAPI-MIME conversion API</span></span>

<span data-ttu-id="12438-113">Dieser Abschnitt enthält Konstantendefinitionen und Klassen- und Schnittstellenbezeichner für die MAPI-MIME-Konversations-API.</span><span class="sxs-lookup"><span data-stu-id="12438-113">This section contains constant definitions and class and interface identifiers for the MAPI-MIME Conversion API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="12438-114">Konstanten</span><span class="sxs-lookup"><span data-stu-id="12438-114">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12438-115">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="12438-115">CCSF_SMTP</span></span>  <br/> |<span data-ttu-id="12438-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="12438-116">0x0002</span></span>  <br/> |
|<span data-ttu-id="12438-117">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="12438-117">CCSF_NOHEADERS</span></span>  <br/> |<span data-ttu-id="12438-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="12438-118">0x0004</span></span>  <br/> |
|<span data-ttu-id="12438-119">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="12438-119">CCSF_USE_TNEF</span></span>  <br/> | <span data-ttu-id="12438-120">0x0010</span><span class="sxs-lookup"><span data-stu-id="12438-120">0x0010</span></span>  <br/> |
|<span data-ttu-id="12438-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="12438-121">CCSF_INCLUDE_BCC</span></span>  <br/> |<span data-ttu-id="12438-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="12438-122">0x0020</span></span>  <br/> |
|<span data-ttu-id="12438-123">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="12438-123">CCSF_8BITHEADERS</span></span>  <br/> | <span data-ttu-id="12438-124">0x0040</span><span class="sxs-lookup"><span data-stu-id="12438-124">0x0040</span></span>  <br/> |
|<span data-ttu-id="12438-125">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="12438-125">CCSF_USE_RTF</span></span>  <br/> |<span data-ttu-id="12438-126">0x0080</span><span class="sxs-lookup"><span data-stu-id="12438-126">0x0080</span></span>  <br/> |
|<span data-ttu-id="12438-127">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="12438-127">CCSF_PLAIN_TEXT_ONLY</span></span>  <br/> |<span data-ttu-id="12438-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="12438-128">0x1000</span></span>  <br/> |
|<span data-ttu-id="12438-129">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="12438-129">CCSF_NO_MSGID</span></span>  <br/> |<span data-ttu-id="12438-130">0x4000</span><span class="sxs-lookup"><span data-stu-id="12438-130">0x4000</span></span>  <br/> |
|<span data-ttu-id="12438-131">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="12438-131">CCSF_GLOBAL_MESSAGE</span></span>  <br/> |<span data-ttu-id="12438-132">0x00200000</span><span class="sxs-lookup"><span data-stu-id="12438-132">0x00200000</span></span>  <br/> |
|<span data-ttu-id="12438-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="12438-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="12438-134">*Wie in der Microsoft Windows Software Development Kit (SDK)-Headerdatei winerror.h definiert*</span><span class="sxs-lookup"><span data-stu-id="12438-134">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="12438-135">Klassenbezeichner</span><span class="sxs-lookup"><span data-stu-id="12438-135">Class identifiers</span></span>

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a><span data-ttu-id="12438-136">Schnittstellenbezeichner</span><span class="sxs-lookup"><span data-stu-id="12438-136">Interface identifiers</span></span>

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a><span data-ttu-id="12438-137">Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="12438-137">Offline State API</span></span>

<span data-ttu-id="12438-138">Dieser Abschnitt enthält Konstantendefinitionen und Klassen- und Schnittstellenbezeichner für die Offlinestatus-API.</span><span class="sxs-lookup"><span data-stu-id="12438-138">This section contains constant definitions and class and interface identifiers for the Offline State API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="12438-139">Konstanten</span><span class="sxs-lookup"><span data-stu-id="12438-139">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12438-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="12438-140">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="12438-141">*Wie in der Microsoft Windows Software Development Kit (SDK)-Headerdatei winerror.h definiert*</span><span class="sxs-lookup"><span data-stu-id="12438-141">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="12438-142">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="12438-142">E_NOINTERFACE</span></span>  <br/> | <span data-ttu-id="12438-143">*Wie in der Windows (SDK)-Headerdatei winerror.h definiert*</span><span class="sxs-lookup"><span data-stu-id="12438-143">*As defined in the Windows (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="12438-144">MAPIOFFLINE_ADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="12438-144">MAPIOFFLINE_ADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="12438-145">(ULONG)0</span><span class="sxs-lookup"><span data-stu-id="12438-145">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="12438-146">MAPIOFFLINE_UNADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="12438-146">MAPIOFFLINE_UNADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="12438-147">(ULONG)0</span><span class="sxs-lookup"><span data-stu-id="12438-147">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="12438-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="12438-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span></span>  <br/> |<span data-ttu-id="12438-149">1</span><span class="sxs-lookup"><span data-stu-id="12438-149">1</span></span>  <br/> |
|<span data-ttu-id="12438-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="12438-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="12438-151">0x1</span><span class="sxs-lookup"><span data-stu-id="12438-151">0x1</span></span>  <br/> |
|<span data-ttu-id="12438-152">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="12438-152">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="12438-153">0x2</span><span class="sxs-lookup"><span data-stu-id="12438-153">0x2</span></span>  <br/> |
|<span data-ttu-id="12438-154">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="12438-154">MAPIOFFLINE_FLAG_BLOCK</span></span>  <br/> |<span data-ttu-id="12438-155">0x00002000</span><span class="sxs-lookup"><span data-stu-id="12438-155">0x00002000</span></span>  <br/> |
|<span data-ttu-id="12438-156">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="12438-156">MAPIOFFLINE_FLAG_DEFAULT</span></span>  <br/> |<span data-ttu-id="12438-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="12438-157">0x00000000</span></span>  <br/> |
|<span data-ttu-id="12438-158">MAPIOFFLINE_STATE_ALL</span><span class="sxs-lookup"><span data-stu-id="12438-158">MAPIOFFLINE_STATE_ALL</span></span>  <br/> |<span data-ttu-id="12438-159">0x003f037f</span><span class="sxs-lookup"><span data-stu-id="12438-159">0x003f037f</span></span>  <br/> |
|<span data-ttu-id="12438-160">**Online oder offline**</span><span class="sxs-lookup"><span data-stu-id="12438-160">**Online or offline**</span></span> <br/> ||
|<span data-ttu-id="12438-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span><span class="sxs-lookup"><span data-stu-id="12438-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span></span>  <br/> |<span data-ttu-id="12438-162">0x00000003</span><span class="sxs-lookup"><span data-stu-id="12438-162">0x00000003</span></span>  <br/> |
|<span data-ttu-id="12438-163">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="12438-163">MAPIOFFLINE_STATE_OFFLINE</span></span>  <br/> |<span data-ttu-id="12438-164">0x00000001</span><span class="sxs-lookup"><span data-stu-id="12438-164">0x00000001</span></span>  <br/> |
|<span data-ttu-id="12438-165">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="12438-165">MAPIOFFLINE_STATE_ONLINE</span></span>  <br/> |<span data-ttu-id="12438-166">0x00000002</span><span class="sxs-lookup"><span data-stu-id="12438-166">0x00000002</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="12438-167">Klassenbezeichner</span><span class="sxs-lookup"><span data-stu-id="12438-167">Class identifiers</span></span>

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a><span data-ttu-id="12438-168">Schnittstellenbezeichner</span><span class="sxs-lookup"><span data-stu-id="12438-168">Interface identifiers</span></span>

```cpp
//{000672B5-0000-0000-c000-000000000046}
DEFINE_GUID(IID_IMAPIOffline, 0x000672B5, 0x0000, 0x0000, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
```

```cpp
//{0317bde5-fc29-44cd-8dcd-36125a3be9ec}
DEFINE_GUID(IID_IMAPIOfflineNotify, 0x0317bde5, 0xfc29, 0x44cd, 0x8d, 0xcd, 0x36, 0x12, 0x5a, 0x3b, 0xe9, 0xec);
```

```cpp
//{42175607-ff3e-4790-bc18-66c8643e6424
DEFINE_GUID(IID_IMAPIOfflineMgr, 0x42175607, 0xFF3E, 0x4790, 0xbc, 0x18, 0x66, 0xc8, 0x64, 0x3e, 0x64, 0x24);
```

## <a name="outlook-named-properties"></a><span data-ttu-id="12438-169">Benannte Eigenschaften Outlook</span><span class="sxs-lookup"><span data-stu-id="12438-169">Outlook named properties</span></span>

<span data-ttu-id="12438-170">Dieser Abschnitt enthält Konstantendefinitionen für benannte Eigenschaften und deren Namespaces sowie andere verwandte Konstanten.</span><span class="sxs-lookup"><span data-stu-id="12438-170">This section contains constant definitions for named properties and their namespaces, and other related constants.</span></span>
  
### <a name="definitions-for-named-properties"></a><span data-ttu-id="12438-171">Definitionen für benannte Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12438-171">Definitions for named properties</span></span>

```cpp
#define dispidMeetingType0x0026 
#define dispidFileUnder0x8005 
#define dispidYomiFirstName 0x802C 
#define dispidYomiLastName 0x802D 
#define dispidYomiCompanyName 0x802E 
#define dispidWorkAddressStreet 0x8045 
#define dispidWorkAddressCity 0x8046 
#define dispidWorkAddressState 0x8047 
#define dispidWorkAddressPostalCode 0x8048 
#define dispidWorkAddressCountry 0x8049 
#define dispidWorkAddressPostOfficeBox 0x804A 
#define dispidInstMsg 0x8062 
#define dispidEmailDisplayName 0x8080 
#define dispidEmailAddrType 0x8082 
#define dispidEmailEmailAddress 0x8083 
#define dispidEmailOriginalDisplayName 0x8084 
#define dispidEmail1OriginalEntryID0x8085 
#define dispidEmail2DisplayName 0x8090 
#define dispidEmail2AddrType 0x8092 
#define dispidEmail2EmailAddress 0x8093 
#define dispidEmail2OriginalDisplayName 0x8094 
#define dispidEmail2OriginalEntryID0x8095 
#define dispidEmail3DisplayName 0x80A0 
#define dispidEmail3AddrType 0x80A2 
#define dispidEmail3EmailAddress 0x80A3 
#define dispidEmail3OriginalDisplayName 0x80A4 
#define dispidEmail3OriginalEntryID0x80A5 
#define dispidTaskStatus 0x8101 
#define dispidTaskStartDate 0x8104 
#define dispidTaskDueDate 0x8105 
#define dispidTaskActualEffort 0x8110 
#define dispidTaskEstimatedEffort 0x8111 
#define dispidTaskFRecur 0x8126 
#define dispidBusyStatus0x8205 
#define dispidLocation 0x8208 
#define dispidApptStartWhole 0x820D 
#define dispidApptEndWhole 0x820E 
#define dispidApptDuration 0x8213 
#define dispidRecurring 0x8223 
#define dispidTimeZoneStruct0x8233 
#define dispidAllAttendeesString 0x8238 
#define dispidToAttendeesString 0x823B 
#define dispidCCAttendeesString 0x823C 
#define dispidConfCheck0x8240 
#define dispidApptCounterProposal 0x8257 
#define dispidApptTZDefStartDisplay0x825E 
#define dispidApptTZDefEndDisplay0x825F 
#define dispidApptTZDefRecur0x8260 
#define dispidReminderTime0x8502 
#define dispidReminderSet 0x8503 
#define dispidFormStorage0x850F 
#define dispidPageDirStream0x8513 
#define dispidSmartNoAttach 0x8514 
#define dispidCommonStart 0x8516 
#define dispidCommonEnd 0x8517 
#define dispidFormPropStream0x851B 
#define dispidRequest 0x8530 
#define dispidCompanies 0x8539 
#define dispidContacts0x853A 
#define dispidPropDefStream0x8540 
#define dispidScriptStream0x8541 
#define dispidCustomFlag0x8542 
#define dispidReminderNextTime 0x8560 
#define dispidHeaderItem0x8578 
#define dispidUseTNEF0x8582 
#define dispidToDoTitle0x85A4 
#define dispidLogType 0x8700 
#define dispidLogStart 0x8706 
#define dispidLogDuration 0x8707 
#define dispidLogEnd 0x8708 
```

### <a name="definitions-for-namespaces"></a><span data-ttu-id="12438-172">Definitionen für Namespaces</span><span class="sxs-lookup"><span data-stu-id="12438-172">Definitions for namespaces</span></span>

<span data-ttu-id="12438-173">Die folgenden Globally Unique Identifiers (GUIDs) repräsentieren die Namespaces der benannten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="12438-173">The following globally unique identifiers (GUIDs) represent the namespaces of the named properties.</span></span>
  
```cpp
const GUID PS_INTERNET_HEADERS  = {0x00020386, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PS_PUBLIC_STRINGS    = {0x00020329, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Appointment= {0x00062002, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Address       = {0x00062004, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Common        = {0x00062008, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Log           = {0x0006200A, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Meeting = {0x6ED8DA90, 0x450B, 0x101B, {0x98, 0xDA, 0x00, 0xAA, 0x00, 0x3F, 0x13, 0x05}}; 
const GUID PSETID_Task          = {0x00062003, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
```

<span data-ttu-id="12438-174">Die PSETID-Definitionen finden Sie im Abschnitt MAPI-Speicher.</span><span class="sxs-lookup"><span data-stu-id="12438-174">Refer to the section MAPI Store for the PSETID definitions.</span></span>
  
### <a name="other-constants"></a><span data-ttu-id="12438-175">Andere Konstanten</span><span class="sxs-lookup"><span data-stu-id="12438-175">Other constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12438-176">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="12438-176">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="12438-177">0xD000000</span><span class="sxs-lookup"><span data-stu-id="12438-177">0xD000000</span></span>  <br/> |
|<span data-ttu-id="12438-178">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="12438-178">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="12438-179">0x2000000</span><span class="sxs-lookup"><span data-stu-id="12438-179">0x2000000</span></span>  <br/> |
|<span data-ttu-id="12438-180">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="12438-180">MNID_ID</span></span>  <br/> | <span data-ttu-id="12438-181">*Wie in der Headerdatei mapidefs.h definiert.*</span><span class="sxs-lookup"><span data-stu-id="12438-181">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="12438-182">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="12438-182">MNID_STRING</span></span>  <br/> | <span data-ttu-id="12438-183">*Wie in der Headerdatei mapidefs.h definiert.*</span><span class="sxs-lookup"><span data-stu-id="12438-183">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="12438-184">mtgNone</span><span class="sxs-lookup"><span data-stu-id="12438-184">mtgNone</span></span>  <br/> |<span data-ttu-id="12438-185">0x0</span><span class="sxs-lookup"><span data-stu-id="12438-185">0x0</span></span>  <br/> |
|<span data-ttu-id="12438-186">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="12438-186">mtgRequest</span></span>  <br/> |<span data-ttu-id="12438-187">0x00000001</span><span class="sxs-lookup"><span data-stu-id="12438-187">0x00000001</span></span>  <br/> |
|<span data-ttu-id="12438-188">mtgFullUpdate</span><span class="sxs-lookup"><span data-stu-id="12438-188">mtgFullUpdate</span></span>  <br/> |<span data-ttu-id="12438-189">0x00010000</span><span class="sxs-lookup"><span data-stu-id="12438-189">0x00010000</span></span>  <br/> |
|<span data-ttu-id="12438-190">mtgInfoUpdate</span><span class="sxs-lookup"><span data-stu-id="12438-190">mtgInfoUpdate</span></span>  <br/> |<span data-ttu-id="12438-191">0x00020000</span><span class="sxs-lookup"><span data-stu-id="12438-191">0x00020000</span></span>  <br/> |
|<span data-ttu-id="12438-192">mtgOutofDate</span><span class="sxs-lookup"><span data-stu-id="12438-192">mtgOutofDate</span></span>  <br/> |<span data-ttu-id="12438-193">0x00080000</span><span class="sxs-lookup"><span data-stu-id="12438-193">0x00080000</span></span>  <br/> |
|<span data-ttu-id="12438-194">mtgDelegated</span><span class="sxs-lookup"><span data-stu-id="12438-194">mtgDelegated</span></span>  <br/> |<span data-ttu-id="12438-195">0x00100000</span><span class="sxs-lookup"><span data-stu-id="12438-195">0x00100000</span></span>  <br/> |
   
## <a name="replication-api"></a><span data-ttu-id="12438-196">Replikations-API</span><span class="sxs-lookup"><span data-stu-id="12438-196">Replication API</span></span>

<span data-ttu-id="12438-197">Dieser Abschnitt enthält die Konstantendefinitionen, MAPI-Schnittstellendeklarationen und Klassen- und Schnittstellenbezeichner für die Replikations-API.</span><span class="sxs-lookup"><span data-stu-id="12438-197">This section contains constant definitions, MAPI interface declarations, and class and interface identifiers for the Replication API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="12438-198">Konstanten</span><span class="sxs-lookup"><span data-stu-id="12438-198">Constants</span></span>

<span data-ttu-id="12438-199">Im folgenden finden Sie eine [MAPIUID](mapiuid.md)-Struktur für die Identifizierung eines MAPI-Dienstanbieters:</span><span class="sxs-lookup"><span data-stu-id="12438-199">The following is a [MAPIUID](mapiuid.md) structure identifying a MAPI service provider:</span></span> 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|<span data-ttu-id="12438-200">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="12438-200">DNH_OK</span></span>  <br/> |<span data-ttu-id="12438-201">0x00010000</span><span class="sxs-lookup"><span data-stu-id="12438-201">0x00010000</span></span>  <br/> |
|<span data-ttu-id="12438-202">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="12438-202">DNT_OK</span></span>  <br/> |<span data-ttu-id="12438-203">0x00010000</span><span class="sxs-lookup"><span data-stu-id="12438-203">0x00010000</span></span>  <br/> |
|<span data-ttu-id="12438-204">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="12438-204">HSF_LOCAL</span></span>  <br/> |<span data-ttu-id="12438-205">0x00000008</span><span class="sxs-lookup"><span data-stu-id="12438-205">0x00000008</span></span>  <br/> |
|<span data-ttu-id="12438-206">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="12438-206">HSF_COPYDESTRUCTIVE</span></span>  <br/> |<span data-ttu-id="12438-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12438-207">0x00000010</span></span>  <br/> |
|<span data-ttu-id="12438-208">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="12438-208">HSF_OK</span></span>  <br/> |<span data-ttu-id="12438-209">0x00010000</span><span class="sxs-lookup"><span data-stu-id="12438-209">0x00010000</span></span>  <br/> |
|<span data-ttu-id="12438-210">MDB_OST_LOGON_UNICODE</span><span class="sxs-lookup"><span data-stu-id="12438-210">MDB_OST_LOGON_UNICODE</span></span>  <br/> |<span data-ttu-id="12438-211">((ULONG) 0x00000800)</span><span class="sxs-lookup"><span data-stu-id="12438-211">((ULONG) 0x00000800)</span></span>  <br/> |
|<span data-ttu-id="12438-212">MDB_OST_LOGON_ANSI</span><span class="sxs-lookup"><span data-stu-id="12438-212">MDB_OST_LOGON_ANSI</span></span>  <br/> |<span data-ttu-id="12438-213">((ULONG) 0x00001000)</span><span class="sxs-lookup"><span data-stu-id="12438-213">((ULONG) 0x00001000)</span></span>  <br/> |
|<span data-ttu-id="12438-214">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="12438-214">SHOW_SOFT_DELETES</span></span>  <br/> |<span data-ttu-id="12438-215">((ULONG) 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="12438-215">((ULONG) 0x00000002)</span></span>  <br/> |
|<span data-ttu-id="12438-216">SS_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="12438-216">SS_ACTIVE</span></span>  <br/> |<span data-ttu-id="12438-217">0</span><span class="sxs-lookup"><span data-stu-id="12438-217">0</span></span>  <br/> |
|<span data-ttu-id="12438-218">SS_SUSPENDED</span><span class="sxs-lookup"><span data-stu-id="12438-218">SS_SUSPENDED</span></span>  <br/> |<span data-ttu-id="12438-219">1</span><span class="sxs-lookup"><span data-stu-id="12438-219">1</span></span>  <br/> |
|<span data-ttu-id="12438-220">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="12438-220">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="12438-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="12438-221">0x00000001</span></span>  <br/> |
|<span data-ttu-id="12438-222">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="12438-222">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="12438-223">0x00000002</span><span class="sxs-lookup"><span data-stu-id="12438-223">0x00000002</span></span>  <br/> |
|<span data-ttu-id="12438-224">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="12438-224">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="12438-225">0x00000040</span><span class="sxs-lookup"><span data-stu-id="12438-225">0x00000040</span></span>  <br/> |
|<span data-ttu-id="12438-226">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="12438-226">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="12438-227">0x00000080</span><span class="sxs-lookup"><span data-stu-id="12438-227">0x00000080</span></span>  <br/> |
|<span data-ttu-id="12438-228">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="12438-228">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="12438-229">0x00000200</span><span class="sxs-lookup"><span data-stu-id="12438-229">0x00000200</span></span>  <br/> |
|<span data-ttu-id="12438-230">SYNC_BACKGROUND</span><span class="sxs-lookup"><span data-stu-id="12438-230">SYNC_BACKGROUND</span></span>  <br/> |<span data-ttu-id="12438-231">0x00001000</span><span class="sxs-lookup"><span data-stu-id="12438-231">0x00001000</span></span>  <br/> |
|<span data-ttu-id="12438-232">SYNC_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="12438-232">SYNC_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="12438-233">0x00020000</span><span class="sxs-lookup"><span data-stu-id="12438-233">0x00020000</span></span>  <br/> |
|<span data-ttu-id="12438-234">SYNC_HEADERS</span><span class="sxs-lookup"><span data-stu-id="12438-234">SYNC_HEADERS</span></span>  <br/> |<span data-ttu-id="12438-235">0x02000000</span><span class="sxs-lookup"><span data-stu-id="12438-235">0x02000000</span></span>  <br/> |
|<span data-ttu-id="12438-236">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="12438-236">UPC_OK</span></span>  <br/> |<span data-ttu-id="12438-237">0x00010000</span><span class="sxs-lookup"><span data-stu-id="12438-237">0x00010000</span></span>  <br/> |
|<span data-ttu-id="12438-238">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="12438-238">UPD_ASSOC</span></span>  <br/> |<span data-ttu-id="12438-239">0x00000001</span><span class="sxs-lookup"><span data-stu-id="12438-239">0x00000001</span></span>  <br/> |
|<span data-ttu-id="12438-240">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="12438-240">UPD_MOV</span></span>  <br/> |<span data-ttu-id="12438-241">0x00000002</span><span class="sxs-lookup"><span data-stu-id="12438-241">0x00000002</span></span>  <br/> |
|<span data-ttu-id="12438-242">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="12438-242">UPD_OK</span></span>  <br/> |<span data-ttu-id="12438-243">0x00010000</span><span class="sxs-lookup"><span data-stu-id="12438-243">0x00010000</span></span>  <br/> |
|<span data-ttu-id="12438-244">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="12438-244">UPD_MOVED</span></span>  <br/> |<span data-ttu-id="12438-245">0x00020000</span><span class="sxs-lookup"><span data-stu-id="12438-245">0x00020000</span></span>  <br/> |
|<span data-ttu-id="12438-246">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="12438-246">UPD_UPDATE</span></span>  <br/> |<span data-ttu-id="12438-247">0x00040000</span><span class="sxs-lookup"><span data-stu-id="12438-247">0x00040000</span></span>  <br/> |
|<span data-ttu-id="12438-248">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="12438-248">UPD_COMMIT</span></span>  <br/> |<span data-ttu-id="12438-249">0x00080000</span><span class="sxs-lookup"><span data-stu-id="12438-249">0x00080000</span></span>  <br/> |
|<span data-ttu-id="12438-250">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="12438-250">UPF_NEW</span></span>  <br/> |<span data-ttu-id="12438-251">0x00000001</span><span class="sxs-lookup"><span data-stu-id="12438-251">0x00000001</span></span>  <br/> |
|<span data-ttu-id="12438-252">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="12438-252">UPF_MOD_PARENT</span></span>  <br/> |<span data-ttu-id="12438-253">0x00000002</span><span class="sxs-lookup"><span data-stu-id="12438-253">0x00000002</span></span>  <br/> |
|<span data-ttu-id="12438-254">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="12438-254">UPF_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="12438-255">0x00000004</span><span class="sxs-lookup"><span data-stu-id="12438-255">0x00000004</span></span>  <br/> |
|<span data-ttu-id="12438-256">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="12438-256">UPF_DEL</span></span>  <br/> |<span data-ttu-id="12438-257">0x00000008</span><span class="sxs-lookup"><span data-stu-id="12438-257">0x00000008</span></span>  <br/> |
|<span data-ttu-id="12438-258">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="12438-258">UPF_OK</span></span>  <br/> |<span data-ttu-id="12438-259">0x00010000</span><span class="sxs-lookup"><span data-stu-id="12438-259">0x00010000</span></span>  <br/> |
|<span data-ttu-id="12438-260">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="12438-260">UPH_OK</span></span>  <br/> |<span data-ttu-id="12438-261">0x00010000</span><span class="sxs-lookup"><span data-stu-id="12438-261">0x00010000</span></span>  <br/> |
|<span data-ttu-id="12438-262">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="12438-262">UPM_ASSOC</span></span>  <br/> |<span data-ttu-id="12438-263">0x00000001</span><span class="sxs-lookup"><span data-stu-id="12438-263">0x00000001</span></span>  <br/> |
|<span data-ttu-id="12438-264">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="12438-264">UPM_NEW</span></span>  <br/> |<span data-ttu-id="12438-265">0x00000002</span><span class="sxs-lookup"><span data-stu-id="12438-265">0x00000002</span></span>  <br/> |
|<span data-ttu-id="12438-266">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="12438-266">UPM_MOV</span></span>  <br/> |<span data-ttu-id="12438-267">0x00000004</span><span class="sxs-lookup"><span data-stu-id="12438-267">0x00000004</span></span>  <br/> |
|<span data-ttu-id="12438-268">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="12438-268">UPM_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="12438-269">0x00000008</span><span class="sxs-lookup"><span data-stu-id="12438-269">0x00000008</span></span>  <br/> |
|<span data-ttu-id="12438-270">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="12438-270">UPM_HEADER</span></span>  <br/> |<span data-ttu-id="12438-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="12438-271">0x00000010</span></span>  <br/> |
|<span data-ttu-id="12438-272">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="12438-272">UPM_OK</span></span>  <br/> |<span data-ttu-id="12438-273">0x00010000</span><span class="sxs-lookup"><span data-stu-id="12438-273">0x00010000</span></span>  <br/> |
|<span data-ttu-id="12438-274">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="12438-274">UPM_MOVED</span></span>  <br/> |<span data-ttu-id="12438-275">0x00020000</span><span class="sxs-lookup"><span data-stu-id="12438-275">0x00020000</span></span>  <br/> |
|<span data-ttu-id="12438-276">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="12438-276">UPM_COMMIT</span></span>  <br/> |<span data-ttu-id="12438-277">0x00040000</span><span class="sxs-lookup"><span data-stu-id="12438-277">0x00040000</span></span>  <br/> |
|<span data-ttu-id="12438-278">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="12438-278">UPM_DELETE</span></span>  <br/> |<span data-ttu-id="12438-279">0x00080000</span><span class="sxs-lookup"><span data-stu-id="12438-279">0x00080000</span></span>  <br/> |
|<span data-ttu-id="12438-280">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="12438-280">UPM_SAVE</span></span>  <br/> |<span data-ttu-id="12438-281">0x00100000</span><span class="sxs-lookup"><span data-stu-id="12438-281">0x00100000</span></span>  <br/> |
|<span data-ttu-id="12438-282">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="12438-282">UPR_ASSOC</span></span>  <br/> |<span data-ttu-id="12438-283">0x00000001</span><span class="sxs-lookup"><span data-stu-id="12438-283">0x00000001</span></span>  <br/> |
|<span data-ttu-id="12438-284">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="12438-284">UPR_READ</span></span>  <br/> |<span data-ttu-id="12438-285">0x00000002</span><span class="sxs-lookup"><span data-stu-id="12438-285">0x00000002</span></span>  <br/> |
|<span data-ttu-id="12438-286">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="12438-286">UPR_OK</span></span>  <br/> |<span data-ttu-id="12438-287">0x00010000</span><span class="sxs-lookup"><span data-stu-id="12438-287">0x00010000</span></span>  <br/> |
|<span data-ttu-id="12438-288">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="12438-288">UPR_COMMIT</span></span>  <br/> |<span data-ttu-id="12438-289">0x00020000</span><span class="sxs-lookup"><span data-stu-id="12438-289">0x00020000</span></span>  <br/> |
|<span data-ttu-id="12438-290">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="12438-290">UPS_UPLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="12438-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="12438-291">0x00000001</span></span>  <br/> |
|<span data-ttu-id="12438-292">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="12438-292">UPS_DNLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="12438-293">0x00000002</span><span class="sxs-lookup"><span data-stu-id="12438-293">0x00000002</span></span>  <br/> |
|<span data-ttu-id="12438-294">UPS_ONE_FOLDER</span><span class="sxs-lookup"><span data-stu-id="12438-294">UPS_ONE_FOLDER</span></span>  <br/> |<span data-ttu-id="12438-295">0x00000004</span><span class="sxs-lookup"><span data-stu-id="12438-295">0x00000004</span></span>  <br/> |
|<span data-ttu-id="12438-296">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="12438-296">UPS_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="12438-297">0x00000080</span><span class="sxs-lookup"><span data-stu-id="12438-297">0x00000080</span></span>  <br/> |
|<span data-ttu-id="12438-298">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="12438-298">UPS_OK</span></span>  <br/> |<span data-ttu-id="12438-299">0x00010000</span><span class="sxs-lookup"><span data-stu-id="12438-299">0x00010000</span></span>  <br/> |
|<span data-ttu-id="12438-300">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="12438-300">UPT_OK</span></span>  <br/> |<span data-ttu-id="12438-301">0x00010000</span><span class="sxs-lookup"><span data-stu-id="12438-301">0x00010000</span></span>  <br/> |
|<span data-ttu-id="12438-302">UPT_PUBLIC</span><span class="sxs-lookup"><span data-stu-id="12438-302">UPT_PUBLIC</span></span>  <br/> |<span data-ttu-id="12438-303">0x00000001</span><span class="sxs-lookup"><span data-stu-id="12438-303">0x00000001</span></span>  <br/> |
|<span data-ttu-id="12438-304">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="12438-304">UPV_ERROR</span></span>  <br/> |<span data-ttu-id="12438-305">0x00010000</span><span class="sxs-lookup"><span data-stu-id="12438-305">0x00010000</span></span>  <br/> |
|<span data-ttu-id="12438-306">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="12438-306">UPV_DIRTY</span></span>  <br/> |<span data-ttu-id="12438-307">0x00020000</span><span class="sxs-lookup"><span data-stu-id="12438-307">0x00020000</span></span>  <br/> |
|<span data-ttu-id="12438-308">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="12438-308">UPV_COMMIT</span></span>  <br/> |<span data-ttu-id="12438-309">0x00040000</span><span class="sxs-lookup"><span data-stu-id="12438-309">0x00040000</span></span>  <br/> |
   
### <a name="interface-declarations"></a><span data-ttu-id="12438-310">Schnittstellendeklarationen</span><span class="sxs-lookup"><span data-stu-id="12438-310">Interface declarations</span></span>

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a><span data-ttu-id="12438-311">Schnittstellenbezeichner</span><span class="sxs-lookup"><span data-stu-id="12438-311">Interface identifiers</span></span>

```cpp
//{4FDEEFF0-0319-11CF-B4CF-00AA0DBBB6E6}
DEFINE_GUID (IID_IPSTX, 0x4FDEEFF0, 0x0319, 0x11CF, 0xB4, 0xCF, 0x00, 0xAA, 0x0D, 0xBB, 0xB6, 0xE6)
```

```cpp
//{2067A790-2A45-11D1-EB86-00A0C90DCA6D}
DEFINE_GUID (IID_IPSTX2, 0x2067A790, 0x2A45, 0x11D1, 0xEB, 0x86, 0x00, 0xA0, 0xC9, 0x0D, 0xCA, 0x6D)
```

```cpp
//{55f15320-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX3, 0x55f15320, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{aa2e2092-ac08-11d2-a2f9-0060b0ec3d4f}
DEFINE_GUID (IID_IPSTX4, 0xaa2e2092, 0xac08, 0x11d2, 0xa2, 0xf9, 0x00, 0x60, 0xb0, 0xec, 0x3d, 0x4f)
```

```cpp
//{55f15322-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX5, 0x55f15322, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{55f15323-111b-11d2-a999-006008b05aa7}
DEFINE_GUID (IID_IPSTX6, 0x55f15323, 0x111b, 0x11d2, 0xa9, 0x99, 0x00, 0x60, 0x08, 0xb0, 0x5a, 0xa7)
```

```cpp
//{d2d85db4-840f-49b8-9982-07d2405ec6b7}
DEFINE_GUID (IID_IOSTX, 0xd2d85db4,  0x840f, 0x49b8, 0x99, 0x82, 0x07, 0xd2, 0x40, 0x5e, 0xc6, 0xb7)
```

<br/>

<span data-ttu-id="12438-312">Verwenden Sie die beiden folgenden Schnittstellenbezeichner [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md) oder [IMsgStore::OpenEntry](imsgstore-openentry.md), um alle Anbieterprüfungen bei einem Ordner- und einem Nachrichtenobjekt  zu öffnen und ignorieren.</span><span class="sxs-lookup"><span data-stu-id="12438-312">Use the two following interface identifiers with [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), or [IMsgStore::OpenEntry](imsgstore-openentry.md) to open and ignore any provider check on a folder object and a message object, respectively.</span></span> 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a><span data-ttu-id="12438-313">MAPI-Speicher</span><span class="sxs-lookup"><span data-stu-id="12438-313">MAPI store</span></span>

<span data-ttu-id="12438-314">Dieser Abschnitt enthält Konstantendefinitionen und Schnittstellenbezeichner, die von APIs mit einer MAPI-Speicher-Schnittstelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12438-314">This section contains constant definitions and interface identifiers used by APIs that interface with a MAPI store.</span></span>
  
### <a name="constants"></a><span data-ttu-id="12438-315">Konstanten</span><span class="sxs-lookup"><span data-stu-id="12438-315">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="12438-316">fnevIndexing</span><span class="sxs-lookup"><span data-stu-id="12438-316">fnevIndexing</span></span>  <br/> |<span data-ttu-id="12438-317">((ULONG) 0x00010000)</span><span class="sxs-lookup"><span data-stu-id="12438-317">((ULONG) 0x00010000)</span></span>  <br/> |<span data-ttu-id="12438-318">Ein Speicheranbieter kann **FnevIndexing** im **UlEventType**-Mitglied der Struktur **[NOTIFICATION](notification.md)** bereitstellen, um den Indexer zu benachrichtigen, dass ein Objekt für die Indizierung bereitsteht.</span><span class="sxs-lookup"><span data-stu-id="12438-318">A store provider can specify **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure to notify the indexer that an object is ready for indexing.</span></span> <span data-ttu-id="12438-319">Das **info**-Mitglied der **NOTIFICATION**-Struktur enthält eine **[EXTENDED_NOTIFICATION](extended_notification.md)**-Struktur.</span><span class="sxs-lookup"><span data-stu-id="12438-319">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="12438-320">FS_NONE</span><span class="sxs-lookup"><span data-stu-id="12438-320">FS_NONE</span></span>  <br/> |<span data-ttu-id="12438-321">0x00</span><span class="sxs-lookup"><span data-stu-id="12438-321">0x00</span></span>  <br/> |<span data-ttu-id="12438-322">Ein Client kann **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** aufrufen und die zurückgegebene Bitmaske überprüfen.</span><span class="sxs-lookup"><span data-stu-id="12438-322">A client can call **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** and check for the returned bitmask.</span></span> <span data-ttu-id="12438-323">**FS_NONE** gibt an, dass der Ordner keine Freigabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12438-323">**FS_NONE** indicates that the folder does not support sharing.</span></span>  <br/> |
|<span data-ttu-id="12438-324">FS_SUPPORTS_SHARING</span><span class="sxs-lookup"><span data-stu-id="12438-324">FS_SUPPORTS_SHARING</span></span>  <br/> |<span data-ttu-id="12438-325">0x01</span><span class="sxs-lookup"><span data-stu-id="12438-325">0x01</span></span>  <br/> |<span data-ttu-id="12438-326">Ein Client kann **IFolderSupport::GetSupportMask** aufrufen und die zurückgegebene Bitmaske überprüfen.</span><span class="sxs-lookup"><span data-stu-id="12438-326">A client can call **IFolderSupport::GetSupportMask** and check for the returned bitmask.</span></span> <span data-ttu-id="12438-327">**FS_SUPPORTS_SHARING** gibt an, dass der Ordner die Freigabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12438-327">**FS_SUPPORTS_SHARING** indicates that the folder supports sharing.</span></span>  <br/> |
|<span data-ttu-id="12438-328">INDEXING_SEARCH_OWNER</span><span class="sxs-lookup"><span data-stu-id="12438-328">INDEXING_SEARCH_OWNER</span></span>  <br/> |<span data-ttu-id="12438-329">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="12438-329">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="12438-330">Gibt den Prozess an, bei dem eine Benachrichtigung an einen Indexer erfolgt, dass ein Objekt für die Indizierung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="12438-330">Identifies the process that is pushing a notification to an indexer that an object is ready for indexing.</span></span>  <br/> |
|<span data-ttu-id="12438-331">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="12438-331">MNID_ID</span></span>  <br/> |<span data-ttu-id="12438-332">Wie in der Microsoft Windows Software Development Kit (SDK)-Headerdatei mapidefs.h definiert</span><span class="sxs-lookup"><span data-stu-id="12438-332">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h</span></span>  <br/> |<span data-ttu-id="12438-333">Einen Wert für das **ulKind**-Feld der **[MAPINAMEID](mapinameid.md)**-Struktur.</span><span class="sxs-lookup"><span data-stu-id="12438-333">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="12438-334">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="12438-334">MNID_STRING</span></span>  <br/> |<span data-ttu-id="12438-335">Wie in der Microsoft Windows Software Development Kit (SDK)-Headerdatei mapidefs.h definiert.</span><span class="sxs-lookup"><span data-stu-id="12438-335">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h.</span></span>  <br/> |<span data-ttu-id="12438-336">Einen Wert für das **ulKind**-Feld der **[MAPINAMEID](mapinameid.md)**-Struktur.</span><span class="sxs-lookup"><span data-stu-id="12438-336">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="12438-337">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="12438-337">MSCAP_RES_ANNOTATION</span></span>  <br/> |<span data-ttu-id="12438-338">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="12438-338">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="12438-339">Wenn ein Client **MSCAP_SEL_RESTRICTION** im *MscapSelector* für **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)** angibt, kann **GetCapabilities** diesen Wert zurückzugeben, wenn der Speicher ungültige Parameter in einer Einschränkung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="12438-339">If a client specifies **MSCAP_SEL_RESTRICTION** in  *mscapSelector*  for **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** can return this value if the store ignores invalid parameters in a restriction.</span></span>  <br/> |
|<span data-ttu-id="12438-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="12438-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>  <br/> |<span data-ttu-id="12438-341">((ULONG) 0x00000020)</span><span class="sxs-lookup"><span data-stu-id="12438-341">((ULONG) 0x00000020)</span></span>  <br/> |<span data-ttu-id="12438-342">Wenn ein Client **MSCAP_SEL_FOLDER** im *MscapSelector* für **IMSCapabilities::GetCapabilities** angibt, kann **GetCapabilities** diesen Wert zurückzugeben, wenn es sich bei dem Speicher um einen nicht standardmäßigen Speicher handelt, der Ordnerhomepages unterstützt. </span><span class="sxs-lookup"><span data-stu-id="12438-342">If a client specifies **MSCAP_SEL_FOLDER** in  *mscapSelector*  for **IMSCapabilities::GetCapabilities**, **GetCapabilities** can return this value if the store is a non-default store that supports folder home pages.</span></span>  <br/> |
|<span data-ttu-id="12438-343">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="12438-343">STORE_PUSHER_OK</span></span>  <br/> |<span data-ttu-id="12438-344">((ULONG) 0x00800000)</span><span class="sxs-lookup"><span data-stu-id="12438-344">((ULONG) 0x00800000)</span></span>  <br/> |<span data-ttu-id="12438-345">Ein Client kann die Eigenschaft **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** abrufen, um das Merkmal eines Nachrichtenspeichers zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="12438-345">A client can get the property **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** to determine the characteristic of a message store.</span></span> <span data-ttu-id="12438-346">Wenn der Speicheranbieter die **STORE_PUSHER_OK**-Kennzeichnung in die Bitmaske einfügt, bedeutet dies, dass der MAPI-Protokollhandler den Speicher nicht durchforstet und der Speicher alle Benachrichtigungen über Änderungen an den Indexer senden muss, damit die Nachrichten indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="12438-346">If the store provider sets the **STORE_PUSHER_OK** flag in the bitmask, that means the MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>  <br/> |
   
### <a name="definitions-for-namespaces"></a><span data-ttu-id="12438-347">Definitionen für Namespaces</span><span class="sxs-lookup"><span data-stu-id="12438-347">Definitions for namespaces</span></span>

<span data-ttu-id="12438-348">Die folgenden Globally Unique Identifiers (GUIDs) repräsentieren die Namespaces benannter Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="12438-348">The following globally unique identifiers (GUIDs) represent the namespaces of named properties.</span></span> <span data-ttu-id="12438-349">Sie werden durch den MAPI Protocol Handler (PH) indiziert und als schreibgeschützt dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="12438-349">They are indexed by the MAPI Protocol Handler (PH), and are documented as read-only.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="12438-350">Die benannten Eigenschaften sollte nicht zum Erstellen oder Ändern von Elementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12438-350">The named properties should not be used to create or modify items.</span></span> 
  
```cpp
const GUID PS_INTERNET_HEADERS  = {0x00020386, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PS_PUBLIC_STRINGS    = {0x00020329, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Address       = {0x00062004, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Appointment   = {0x00062002, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Common        = {0x00062008, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Log           = {0x0006200A, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
const GUID PSETID_Meeting       = {0x6ED8DA90, 0x450B, 0x101B, {0x98, 0xDA, 0x00, 0xAA, 0x00, 0x3F, 0x13, 0x05}}; 
const GUID PSETID_Task          = {0x00062003, 0x0000, 0x0000, {0xC0, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x46}}; 
```

#### <a name="mnid_id-properties"></a><span data-ttu-id="12438-351">MNID_ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12438-351">MNID_ID Properties</span></span>
  
```cpp
// In PSETID_Address
#define dispidWorkAddressStreet 0x8045
#define dispidWorkAddressCity 0x8046
#define dispidWorkAddressState 0x8047
#define dispidWorkAddressPostalCode 0x8048
#define dispidWorkAddressCountry 0x8049
#define dispidInstMsg 0x8062
#define dispidEmailDisplayName 0x8080
#define dispidEmailOriginalDisplayName 0x8084
```

```cpp
// In PSETID_Appointment
#define dispidLocation 0x8208
#define dispidApptStartWhole 0x820D
#define dispidApptEndWhole 0x820E
#define dispidApptDuration 0x8213
#define dispidRecurring 0x8223
#define dispidAllAttendeesString 0x8238
#define dispidToAttendeesString 0x823B
#define dispidCCAttendeesString 0x823C
```

```cpp
// In PSETID_Common
#define dispidReminderSet 0x8503
#define dispidSmartNoAttach 0x8514
#define dispidCommonStart 0x8516
#define dispidCommonEnd 0x8517
#define dispidRequest 0x8530
#define dispidCompanies 0x8539
#define dispidReminderNextTime 0x8560
```

```cpp
// In PSETID_Log (also known as Journal)
#define dispidLogType 0x8700
#define dispidLogStart 0x8706
#define dispidLogDuration 0x8707
#define dispidLogEnd 0x8708MNID_STRING properties
```

```cpp
// In PSETID_Task
#define dispidTaskStartDate 0x8104
#define dispidTaskDueDate 0x8105
#define dispidTaskActualEffort 0x8110
#define dispidTaskEstimatedEffort 0x8111
#define dispidTaskFRecur 0x8126
```

#### <a name="mnid_string-properties"></a><span data-ttu-id="12438-352">MNID_STRING-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12438-352">MNID_STRING Properties</span></span>
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a><span data-ttu-id="12438-353">Schnittstellenbezeichner</span><span class="sxs-lookup"><span data-stu-id="12438-353">Interface identifiers</span></span>

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

<span data-ttu-id="12438-354">Verwenden Sie das in der Windows SDK-Headerdatei guiddef.h definierte `DEFINE_OLEGUID`-Makro, um den folgenden symbolischen GUID-Namen seinem Wert zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="12438-354">Use the  `DEFINE_OLEGUID` macro defined in the Windows SDK header file guiddef.h to associate the following GUID symbolic name with its value.</span></span> 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a><span data-ttu-id="12438-355">MAPI-Adressbuch-Konstanten</span><span class="sxs-lookup"><span data-stu-id="12438-355">MAPI Address Book constants</span></span>

<span data-ttu-id="12438-356">Dieser Abschnitt enthält Definitionen für das MAPI-Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="12438-356">This section contains constant definitions for the MAPI Address Book.</span></span>
  
### <a name="constants"></a><span data-ttu-id="12438-357">Konstanten</span><span class="sxs-lookup"><span data-stu-id="12438-357">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="12438-358">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="12438-358">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="12438-359">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="12438-359">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="12438-360">Der Stammordner für ein MAPI-Adressbuch-Objekt.</span><span class="sxs-lookup"><span data-stu-id="12438-360">The root folder for a MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="12438-361">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="12438-361">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="12438-362">((ULONG) 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="12438-362">((ULONG) 0x00000002)</span></span>  <br/> |<span data-ttu-id="12438-363">Ein im Stammordner des MAPI-Adressbuch-Objekts enthaltener Unterordner.</span><span class="sxs-lookup"><span data-stu-id="12438-363">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="12438-364">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="12438-364">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="12438-365">((ULONG) 0x00000003)</span><span class="sxs-lookup"><span data-stu-id="12438-365">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="12438-366">Ein Adressbuchcontainer-Objekt.</span><span class="sxs-lookup"><span data-stu-id="12438-366">An address book container object.</span></span>  <br/> |
|<span data-ttu-id="12438-367">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="12438-367">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="12438-368">((ULONG) 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="12438-368">((ULONG) 0x00000004)</span></span>  <br/> |<span data-ttu-id="12438-369">Ein Nachrichtenbenutzer-Objekt.</span><span class="sxs-lookup"><span data-stu-id="12438-369">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="12438-370">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="12438-370">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="12438-371">((ULONG) 0x00000005)</span><span class="sxs-lookup"><span data-stu-id="12438-371">((ULONG) 0x00000005)</span></span>  <br/> |<span data-ttu-id="12438-372">Ein Verteilerliste-Objekte.</span><span class="sxs-lookup"><span data-stu-id="12438-372">A distribution list object.</span></span>  <br/> |
   
## <a name="additional-mapi-constants"></a><span data-ttu-id="12438-373">Zusätzliche MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="12438-373">Additional MAPI constants</span></span>

<span data-ttu-id="12438-374">Dieser Abschnitt enthält Konstantendefinitionen, einschließlich Fehlercodes, und Schnittstellenbezeichner, die von MAPI-APIs verwendet werden, die zuvor nicht verfügbar gemacht und dokumentiert wurden.</span><span class="sxs-lookup"><span data-stu-id="12438-374">This section contains constant definitions including error codes, and interface identifiers used by MAPI APIs that were not previously exposed and documented.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="12438-375">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="12438-375">DIALOG_MODAL</span></span>  <br/> |<span data-ttu-id="12438-376">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="12438-376">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="12438-377">Wenn ein Client die [IAddrBook::Details](iaddrbook-details.md)-Methode aufruft, muss der Client die **DIALOG_MODAL**-Kennzeichnung im _UlFlags_-Parameter festlegen, um das modale Dialogfeld mit Details zu einem bestimmten Adressbucheintrag anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="12438-377">When a client calls the [IAddrBook::Details](iaddrbook-details.md) method, the client must set the **DIALOG_MODAL** flag in the  _ulFlags_ parameter to display the modal dialog box showing the details about a particular address book entry.</span></span> <span data-ttu-id="12438-378">Diese Konstante wird in mapidefs.h definiert.</span><span class="sxs-lookup"><span data-stu-id="12438-378">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="12438-379">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="12438-379">ITEMPROC_FORCE</span></span>  <br/> |<span data-ttu-id="12438-380">0x00000800</span><span class="sxs-lookup"><span data-stu-id="12438-380">0x00000800</span></span>  <br/> |<span data-ttu-id="12438-381">In Outlook 2007 wenden umschlossene PST-Speicher Regeln und Spamfilter auf neue Nachrichten an, bevor MAPI-Clients über die neuen Nachrichten informiert werden.</span><span class="sxs-lookup"><span data-stu-id="12438-381">In Outlook 2007, wrapped PST stores have rules and spam filtering processed on new messages before MAPI clients are notified of the new messages.</span></span> <span data-ttu-id="12438-382">Ein Anbieter oder Client, der die [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)-Methode verwendet, um eine neue Nachricht in PST-Speichern zu erstellen, sollte die **ITEMPROC_FORCE**-Kennzeichnung im _UlFlags_-Parameter der [IMAPIProp::SaveChanges](imapiprop-savechanges.md)-Methode festlegen, um dem PST-Speicher mitzuteilen, dass die Nachricht zur Regelverarbeitung berechtigt ist, bevor der Speicher einen überwachenden Client über die Ankunft der Nachricht informiert.</span><span class="sxs-lookup"><span data-stu-id="12438-382">A provider or client using the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create a new message in PST stores should set the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to indicate to the PST store that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="12438-383">Beachten Sie, dass diese Regelverarbeitung sich nur auf neue, auf einem anderen als einem Microsoft Exchange Server erstellte Nachrichten bezieht, da Exchange-Server Regeln für Nachrichten auf dem Server verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="12438-383">Note that such rules processing only applies to new messages created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="12438-384">Der Anbieter oder Client, der die Nachricht erstellt, muss diese Kennzeichnung zusammen mit **NON_EMS_XP_SAVE** übergeben, um anzugeben, dass es sich nicht um einen Exchange-Server handelt.</span><span class="sxs-lookup"><span data-stu-id="12438-384">Hence the provider or client creating the message must pass this flag in combination with **NON_EMS_XP_SAVE**, which indicates the server is not an Exchange server.</span></span>  <br/> |
| <span data-ttu-id="12438-385">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="12438-385">MAPI_BG_SESSION</span></span>  <br/> |<span data-ttu-id="12438-386">0x00200000</span><span class="sxs-lookup"><span data-stu-id="12438-386">0x00200000</span></span>  <br/> |<span data-ttu-id="12438-387">Ein Client kann die [MAPILogonEx](mapilogonex.md)-Funktion aufrufen und die **MAPI_BG_SESSION**-Kennzeichnung im _flFlags_-Parameter einstellen, um sich bei einer Sitzung anzumelden und alle Vorgänge im Hintergrund auszuführen.</span><span class="sxs-lookup"><span data-stu-id="12438-387">A client can call the [MAPILogonEx](mapilogonex.md) function, setting the **MAPI_BG_SESSION** flag in the  _flFlags_ parameter to log on to a session and carry out any operations in the background.</span></span> <span data-ttu-id="12438-388">Wenn ein Client eine Verarbeitung in einem Hintergrund-Thread oder separaten Prozess in einer Weise plant, die den Thread im Vordergrund nicht stört, sollte [MAPILogonEx](mapilogonex.md) mit der **MAPI_BG_SESSION**-Kennzeichnung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="12438-388">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call [MAPILogonEx](mapilogonex.md) with the **MAPI_BG_SESSION** flag.</span></span> <span data-ttu-id="12438-389">Dies ist beispielsweise bei einer Clientanwendung wie der Indizierungs-Engine der Fall, bei der eine Persönliche Ordner-Datei (PST) für den Zugriff im Hintergrund geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="12438-389">An example where this is used is a client application, such as an indexing engine, opening a Personal Folders File (PST) for background type access.</span></span>  <br/> |
|<span data-ttu-id="12438-390">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="12438-390">MAPI_CACHE_ONLY</span></span>  <br/> |<span data-ttu-id="12438-391">0x00004000</span><span class="sxs-lookup"><span data-stu-id="12438-391">0x00004000</span></span>  <br/> |<span data-ttu-id="12438-392">Ein Client kann die [IAddrBook::OpenEntry](iaddrbook-openentry.md)-Methode aufrufen und die **MAPI_CACHE_ONLY**-Kennzeichnung im _ulFlags_-Parameter festlegen, um einen Adressbucheintrag zu öffnen und ausschließlich aus dem Cache darauf zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="12438-392">A client can call the [IAddrBook::OpenEntry](iaddrbook-openentry.md) method, setting the **MAPI_CACHE_ONLY** flag in the  _ulFlags_ parameter to open an address book entry and to access it subsequently only from the cache.</span></span> <span data-ttu-id="12438-393">Ein Beispiel für diese Anwendung ist eine Clientanwendung, mit der die globale Adressliste im Exchange-Cache-Modus geöffnet und aus dem Cache auf einen Eintrag in diesem Adressbuch zugegriffen werden soll, ohne Datenverkehr zwischen dem Client und dem Server zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="12438-393">An example where this is used is a client application that wants to open the Global Address List in Cached Exchange mode and access an entry in that Address Book from the cache without creating traffic between the client and the server.</span></span>  <br/> |
|<span data-ttu-id="12438-394">MAPI_DIALOG_MODELESS</span><span class="sxs-lookup"><span data-stu-id="12438-394">MAPI_DIALOG_MODELESS</span></span>  <br/> |<span data-ttu-id="12438-395">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="12438-395">0x0000000C</span></span>  <br/> |<span data-ttu-id="12438-396">Dieser Wert kann an die MAPISendMail-Funktion von Simple MAPI im _ulFlags_-Parameter übergeben werden, um anzugeben, dass ein nicht modales Dialogfeld von der standardmäßigen E-Mail-Anwendung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="12438-396">This value can be passed to the Simple MAPI MAPISendMail function in the  _ulFlags_ parameter to specify that a modeless dialog box is displayed by the default mail application.</span></span> <span data-ttu-id="12438-397">Wenn weder diese Kennzeichnung noch MAPI_DIALOG (0 x 00000008) festgelegt wird, wird das Dialogfeld nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="12438-397">If neither this flag nor MAPI_DIALOG (0x00000008) is set, no dialog box is displayed.</span></span>  <br/> |
|<span data-ttu-id="12438-398">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="12438-398">MAPI_NO_CACHE</span></span>  <br/> |<span data-ttu-id="12438-399">0x00000200</span><span class="sxs-lookup"><span data-stu-id="12438-399">0x00000200</span></span>  <br/> |<span data-ttu-id="12438-400">Wenn sich Microsoft Office Outlook im Exchange-Cache-Modus befindet und der Speicher im Cache-Modus geöffnet wurde, kann ein Client oder Dienstanbieter [IMsgStore::OpenEntry](imsgstore-openentry.md) aufrufen und die **MAPI_NO_CACHE**-Kennzeichnung im _ulFlags_-Parameter festlegen, um ein Element oder einen Ordner auf dem Remotespeicher zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="12438-400">If Microsoft Office Outlook is in Cached Exchange Mode and a store has been opened in cached mode, a client or service provider can call [IMsgStore::OpenEntry](imsgstore-openentry.md), setting the **MAPI_NO_CACHE** flag in the  _ulFlags_ parameter to open an item or a folder on the remote store.</span></span> <span data-ttu-id="12438-401">Hinweise: Wenn Sie den Nachrichtenspeicher mit der **MDB_ONLINE**-Kennzeichnung auf dem Remoteserver öffnen, brauchen Sie die **MAPI_NO_CACHE**-Kennzeichnung nicht zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="12438-401">Note that if you open the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span>  <br/> |
|<span data-ttu-id="12438-402">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="12438-402">MAPI_UNICODE</span></span>  <br/> |<span data-ttu-id="12438-403">0x80000000</span><span class="sxs-lookup"><span data-stu-id="12438-403">0x80000000</span></span>  <br/> |<span data-ttu-id="12438-404">Ein Client oder Dienstanbieter kann die [OpenIMsgOnIStg](openimsgonistg.md)-Funktion aufrufen und die **MAPI_UNICODE**-Kennzeichnung im _ulFlags_-Parameter einstellen, um  Unicode-MSG-Dateien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="12438-404">A client or service provider can call the [OpenIMsgOnIStg](openimsgonistg.md) function, setting the **MAPI_UNICODE** flag in the  _ulFlags_ parameter to create Unicode .msg files.</span></span> <span data-ttu-id="12438-405">Die sich daraus ergebende [IMessage: IMAPIProp](imessageimapiprop.md)-Datei zeigt **STORE_UNICODE_OK** in der [kanonischen Eigenschaft PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) an und unterstützt Unicode-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="12438-405">The resulting [IMessage : IMAPIProp](imessageimapiprop.md) file shows **STORE_UNICODE_OK** in its [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> <span data-ttu-id="12438-406">Diese Konstante wird in mapidefs.h definiert.</span><span class="sxs-lookup"><span data-stu-id="12438-406">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="12438-407">MDB_ONLINE</span><span class="sxs-lookup"><span data-stu-id="12438-407">MDB_ONLINE</span></span>  <br/> |<span data-ttu-id="12438-408">0x00000100</span><span class="sxs-lookup"><span data-stu-id="12438-408">0x00000100</span></span>  <br/> |<span data-ttu-id="12438-409">Wenn sich Outlook im Exchange-Cache-Modus befindet, kann ein Client oder Dienstanbieter die [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)-Methode aufrufen und die **MDB_ONLINE**-Kennzeichnung im _ulFlags_-Parameter festlegen, um die Verbindung mit dem lokalen Nachrichtenspeicher zu überschreiben und den Speicher auf dem Remoteserver zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="12438-409">If Outlook is in Cached Exchange Mode, a client or service provider can call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method, setting the **MDB_ONLINE** flag in the  _ulFlags_ parameter to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="12438-410">Beachten Sie, dass Sie einen Exchange-Speicher innerhalb der gleichen MAPI-Sitzung nicht gleichzeitig im Cache-Modus und im Nicht-Cache-Modus öffnen können.</span><span class="sxs-lookup"><span data-stu-id="12438-410">Note that you cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="12438-411">Wenn Sie den zwischengespeicherten Nachrichtenspeicher bereits geöffnet haben, müssen Sie entweder den Speicher schließen, bevor Sie ihn mit dieser Kennzeichnung öffnen, oder eine neue MAPI-Sitzung öffnen, in der Sie den Exchange-Speicher auf dem Remoteserver mit dieser Kennzeichnung öffnen können.</span><span class="sxs-lookup"><span data-stu-id="12438-411">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>  <br/> |
|<span data-ttu-id="12438-412">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="12438-412">NON_EMS_XP_SAVE</span></span>  <br/> |<span data-ttu-id="12438-413">0x00001000</span><span class="sxs-lookup"><span data-stu-id="12438-413">0x00001000</span></span>  <br/> |<span data-ttu-id="12438-414">Ein Client kann die [IMAPIProp::SaveChanges](imapiprop-savechanges.md)-Methode mit der **NON_EMS_XP_SAVE**-Kennzeichnung im _ulFlags_-Parameter festlegen, um anzugeben, dass die Nachricht nicht von einem Exchange-Server gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="12438-414">A client can call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method, setting the **NON_EMS_XP_SAVE** flag in the  _ulFlags_ parameter to indicate that the message has not been delivered from an Exchange server.</span></span> <span data-ttu-id="12438-415">Diese Kennzeichnung sollt in Verbindung mit der **ITEMPROC_FORCE**-Kennzeichnung im _ulFlags_-Parameter verwendet werden, um einen PST-Speicher darauf hinzuweisen, dass die Nachricht für die Regelverarbeitung berechtigt ist, bevor der PST-Speicher einen überwachenden Client über die Ankunft der Nachricht informiert.</span><span class="sxs-lookup"><span data-stu-id="12438-415">This flag should be used in combination with the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter to indicate to a PST store that the message is eligible for rules processing before the PST store notifies any listening client of the arrival of the message.</span></span> <span data-ttu-id="12438-416">Diese Regelverarbeitung gilt nur für neue Nachrichten, die mit [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) auf einem anderen Server als dem Exchange-Server erstellt wurden (da der Exchange-Server bereits die Regelverarbeitung vorgenommen hätte).</span><span class="sxs-lookup"><span data-stu-id="12438-416">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange server (in which case the Exchange server would have already processed rules on the message).</span></span>  <br/> |
|<span data-ttu-id="12438-417">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="12438-417">SPAMFILTER_ONSAVE</span></span>  <br/> |<span data-ttu-id="12438-418">0x00000080</span><span class="sxs-lookup"><span data-stu-id="12438-418">0x00000080</span></span>  <br/> |<span data-ttu-id="12438-419">Ein Client kann [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufrufen und die **SPAMFILTER_ONSAVE**-Kennzeichnung im _ulFlags_-Parameter festlegen, um einen Spamfilter auf die gespeicherte Nachricht anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="12438-419">A client can call [IMAPIProp::SaveChanges](imapiprop-savechanges.md), setting the **SPAMFILTER_ONSAVE** flag in the  _ulFlags_ parameter to enable spam filtering on a message that is being saved.</span></span> <span data-ttu-id="12438-420">Spamfilter-Unterstützung ist nur verfügbar, wenn der E-Mail-Adressentyp des Absenders Simple Mail Transfer Protocol (SMTP) ist und die Nachricht auf einem Speicher für eine Persönliche Ordner-Datei (PST) gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="12438-420">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>  <br/> |
|<span data-ttu-id="12438-421">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="12438-421">STORE_ITEMPROC</span></span>  <br/> |<span data-ttu-id="12438-422">0x00200000</span><span class="sxs-lookup"><span data-stu-id="12438-422">0x00200000</span></span>  <br/> |<span data-ttu-id="12438-423">Wenn diese Kennzeichnung in der [kanonischen Eigenschaft PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) eines umschlossenen PST-Speichers festgelegt wird, bedeutet dies, dass der Speicher beim Eintreffen einer neuen Nachricht Regeln und Spamfilter auf die Nachricht anwendet.</span><span class="sxs-lookup"><span data-stu-id="12438-423">If this flag is set in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) of a wrapped PST store, it indicates that when a new message arrives at the store, the store has rules and spam filtering processed on the message separately.</span></span> <span data-ttu-id="12438-424">Anschließend ruft der Speicher [IMAPISupport::Notify](imapisupport-notify.md) auf und legt **FnevNewMail** in der [NOTIFICATION](notification.md)-Struktur fest, was als Parameter übergeben wird. Die Details der neuen Nachricht werden an einen überwachenden Client weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="12438-424">The store then calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and passing the details of the new message to a listening client.</span></span> <span data-ttu-id="12438-425">Wenn der überwachende Client die Nachricht erhält, wendet er keine Regeln darauf an.</span><span class="sxs-lookup"><span data-stu-id="12438-425">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span>  <br/> |
|<span data-ttu-id="12438-426">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="12438-426">STORE_UNICODE_OK</span></span>  <br/> |<span data-ttu-id="12438-427">0x00040000</span><span class="sxs-lookup"><span data-stu-id="12438-427">0x00040000</span></span>  <br/> |<span data-ttu-id="12438-428">Wenn diese Kennzeichnung in der [kanonischen Eigenschaft PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) enthalten ist, bedeutet dies, dass der Speicher Unicode-Speicherung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12438-428">If this flag is included in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md), it indicates that the store supports Unicode storage.</span></span> <span data-ttu-id="12438-429">Ein Client kann das Vorhandensein dieser Kennzeichnung überprüfen und entscheiden, ob er Unicode-Informationen abruft oder speichert.</span><span class="sxs-lookup"><span data-stu-id="12438-429">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span>  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a><span data-ttu-id="12438-430">Definitionen zum Archivieren von Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="12438-430">Definitions for archiving items in a folder</span></span>

<span data-ttu-id="12438-431">Die folgenden Konstantendefinitionen sind Werte, die verwendet werden, um die [kanonische Eigenschaft PidTagAgingGranularity](pidtagaginggranularity-canonical-property.md) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="12438-431">The following constant definitions are values used to set the [PidTagAgingGranularity Canonical Property](pidtagaginggranularity-canonical-property.md).</span></span>
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a><span data-ttu-id="12438-432">Definitionen zum Anzeigen von Remoteobjekten</span><span class="sxs-lookup"><span data-stu-id="12438-432">Definitions for displaying remote objects</span></span>

<span data-ttu-id="12438-433">Die folgenden Konstanten- und Makrodefinitionen dienen zum Anzeigen von Remoteobjekten.</span><span class="sxs-lookup"><span data-stu-id="12438-433">The following constant and macro definitions are for displaying remote objects.</span></span> <span data-ttu-id="12438-434">Weitere Informationen finden Sie unter [Kanonische Eigenschaft PidTagDisplayTypeEx](pidtagdisplaytypeex-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="12438-434">For more information, see the [PidTagDisplayTypeEx Canonical Property](pidtagdisplaytypeex-canonical-property.md).</span></span>
  
```cpp
#define DTE_FLAG_REMOTE_VALID0x80000000 
#define DTE_FLAG_ACL_CAPABLE    0x40000000 
#define DTE_MASK_REMOTE        0x0000ff00 
#define DTE_MASK_LOCAL        0x000000ff 
  
#define DTE_IS_REMOTE_VALID(v)(!!((v) & DTE_FLAG_REMOTE_VALID)) 
#define DTE_IS_ACL_CAPABLE(v)(!!((v) & DTE_FLAG_ACL_CAPABLE)) 
#define DTE_REMOTE(v)(((v) & DTE_MASK_REMOTE) >> 8) 
#define DTE_LOCAL(v)((v) & DTE_MASK_LOCAL) 
  
#define DT_ROOM((ULONG) 0x00000007) 
#define DT_EQUIPMENT((ULONG) 0x00000008) 
#define DT_SEC_DISTLIST((ULONG) 0x00000009)
```

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a><span data-ttu-id="12438-435">Definitionen für Exchange-Adressbuch- und Message Store-Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="12438-435">Definitions for Exchange address book and Message store error codes</span></span>

<span data-ttu-id="12438-436">Nachfolgend finden Sie Fehlercode-Definitionen für das Exchange-Adressbuch und Message Store, die über eine Verbindungswiederherstellungsfunktion verfügen.</span><span class="sxs-lookup"><span data-stu-id="12438-436">The following contains error code definitions for the Exchange Address Book and Message Store, which have reconnection capability.</span></span> <span data-ttu-id="12438-437">Der letzte Aufruf an einen nicht verbundenen Global Catalog (GC) kann zu einem **MAPI_E_END_OF_SESSION**-Fehler führen, sodass eine Wiederherstellung der Verbindung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="12438-437">The last call to a disconnected Global Catalog (GC) may result in the **MAPI_E_END_OF_SESSION** error, which would need to be retried.</span></span> 
  
<span data-ttu-id="12438-438">Outlook-MAPI unterstützt die erneute Verbindung mit einem globalen Katalogserver, ohne dass eine spezielle Neukonfiguration erforderlich ist, aber es können andere Fehlercodes an den Client zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="12438-438">Outlook's MAPI supports reconnection to a GC server without special reconfiguration, but some other error codes can be returned to the client.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="12438-439">MAPI_E_END_OF_SESSION</span><span class="sxs-lookup"><span data-stu-id="12438-439">MAPI_E_END_OF_SESSION</span></span>  <br/> |<span data-ttu-id="12438-440">0x80040200</span><span class="sxs-lookup"><span data-stu-id="12438-440">0x80040200</span></span>  <br/> |<span data-ttu-id="12438-441">Wird zurückgegeben, wenn eine Verbindung getrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="12438-441">Returned when a connection has been disconnected.</span></span>  <br/> |
|<span data-ttu-id="12438-442">MAPI_E_RECONNECTED</span><span class="sxs-lookup"><span data-stu-id="12438-442">MAPI_E_RECONNECTED</span></span>  <br/> |<span data-ttu-id="12438-443">0x80040125</span><span class="sxs-lookup"><span data-stu-id="12438-443">0x80040125</span></span>  <br/> |<span data-ttu-id="12438-444">Wird zurückgegeben, wenn das Verbindungstoken Remote Procedure Call (RPC) nicht mehr aktuell ist.</span><span class="sxs-lookup"><span data-stu-id="12438-444">Returned when the Remote Procedure Call (RPC) connection token is out-of-date.</span></span> <span data-ttu-id="12438-445">Wenn das Token der aktuellen Transaktion vom Token der Verbindung abweicht, bedeutet dies, dass die Verbindung unterbrochen wurde. **MAPI_E_RECONNECTED** wird zurückgegeben und kann auf die gleiche Weise wie **MAPI_E_END_OF_SESSION** behoben werden.</span><span class="sxs-lookup"><span data-stu-id="12438-445">If the token of the current transaction is different from the token of the connection that means it has reconnected, so **MAPI_E_RECONNECTED** is returned and can be treated the same as **MAPI_E_END_OF_SESSION**.</span></span> <span data-ttu-id="12438-446">Der Aufruf sollte wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="12438-446">The call should be retried.</span></span>  <br/> |
|<span data-ttu-id="12438-447">MAPI_E_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="12438-447">MAPI_E_OFFLINE</span></span>  <br/> |<span data-ttu-id="12438-448">0x80040126</span><span class="sxs-lookup"><span data-stu-id="12438-448">0x80040126</span></span>  <br/> |<span data-ttu-id="12438-449">Wird zurückgegeben, wenn die Verbindung offline ist.</span><span class="sxs-lookup"><span data-stu-id="12438-449">Returned when the connection is offline.</span></span> <span data-ttu-id="12438-450">In der Regel bedeutet dies, dass sich etwas in der Umgebung ereignet hat, z. B. ein Serverfehler oder den Verlust der Netzwerkkonnektivität.</span><span class="sxs-lookup"><span data-stu-id="12438-450">Typically this means that something has occurred in the environment, such as server failure or loss of network connectivity.</span></span> <span data-ttu-id="12438-451">Dieser Fehler tritt meistens auf, wenn Sie ein Cache-Modus-Profil verwenden und versuchen, den Cache für die Kommunikation mit dem Server zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="12438-451">This error is most likely to occur when using a cached mode profile and attempting to bypass the cache to communicate with the server.</span></span> <span data-ttu-id="12438-452">Wenn der Cache nie in der Lage war, eine Verbindung zum Server herzustellen, kann er sich im Status "offline" befinden, sodass **MAPI_E_OFFLINE** ausgegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="12438-452">If the cache was never able to initially establish a connection to the server, it may be in the offline state in which **MAPI_E_OFFLINE** could surface.</span></span>  <br/> |
   
<span data-ttu-id="12438-453">Keiner der beiden vorherigen Fehler wird in Szenarien zurückgegeben, in denen sie normalerweise auftreten würden.</span><span class="sxs-lookup"><span data-stu-id="12438-453">Neither of the preceding two errors will be returned in all scenarios where they would likely appear to apply.</span></span> <span data-ttu-id="12438-454">In den meisten Fällen wird **MAPI\_E_NETWORK_ERROR** oder **MAPI_E_CALL_FAILED** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="12438-454">In most cases, **MAPI\_E_NETWORK_ERROR** or **MAPI_E_CALL_FAILED** will be returned.</span></span> <span data-ttu-id="12438-455">Keiner tritt bei der Verwendung des Downloads [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](https://support.microsoft.com/kb/171440) auf.</span><span class="sxs-lookup"><span data-stu-id="12438-455">Neither will appear using the [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](https://support.microsoft.com/kb/171440) download.</span></span> 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a><span data-ttu-id="12438-456">Definitionen für Exchange Server-Postfach-Cache-Modus-Kontingente</span><span class="sxs-lookup"><span data-stu-id="12438-456">Definitions for Exchange Server Mailbox cached mode quotas</span></span>

<span data-ttu-id="12438-457">Die folgenden Konstantendefinitionen werden von Microsoft Outlook 2010 und Microsoft Outlook 2013 verwendet, um die Exchange-Cache-Modus-Profilkontingente festzulegen, die den Exchange-Postfachkontingenten entsprechen und andernfalls nur mit einem Online-Profil verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="12438-457">The following constant definitions are used by Microsoft Outlook 2010 and Microsoft Outlook 2013 to set the Exchange cached mode profile quotas that are equivalent to the Exchange mailbox quotas otherwise available only with an online profile.</span></span>
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

<span data-ttu-id="12438-458">Diese Eigenschaften sind den entsprechenden Online-Eigenschaften zugeordnet und enthalten dieselben Werte in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="12438-458">These properties map to their correspondent online properties and contain the same values in kilobytes.</span></span> <span data-ttu-id="12438-459">PR_QUOTA_WARNING entspricht PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND entspricht PR_QUOTA_PROHIBIT_SEND_QUOTA und PR_QUOTA_RECEIVE entspricht PR_PROHIBIT_RECEIVE_QUOTA.</span><span class="sxs-lookup"><span data-stu-id="12438-459">PR_QUOTA_WARNING maps to PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND to PR_QUOTA_PROHIBIT_SEND_QUOTA, and PR_QUOTA_RECEIVE to PR_PROHIBIT_RECEIVE_QUOTA.</span></span>
  
### <a name="definitions-for-message-format"></a><span data-ttu-id="12438-460">Definitionen für Nachrichtenformat</span><span class="sxs-lookup"><span data-stu-id="12438-460">Definitions for message format</span></span>

<span data-ttu-id="12438-461">Die folgenden Konstantendefinitionen sind Werte, die verwendet werden, um die [kanonische Eigenschaft PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="12438-461">The following constant definitions are values that are used to set the [PidTagMessageEditorFormat Canonical Property](pidtagmessageeditorformat-canonical-property.md).</span></span>
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a><span data-ttu-id="12438-462">Definitionen für die Verwendung von RPC über HTTP</span><span class="sxs-lookup"><span data-stu-id="12438-462">Definitions for using RPC over HTTP</span></span>

<span data-ttu-id="12438-463">Unter [kanonische Eigenschaft PidTagRpcOverHttpFlags](pidtagrpcoverhttpflags-canonical-property.md) finden Sie Konstantendefinitionen, die als Kennzeichnungen zum Festlegen der Eigenschaft verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12438-463">See the [PidTagRpcOverHttpFlags Canonical Property](pidtagrpcoverhttpflags-canonical-property.md) topic for constant definitions used as flags to set the property.</span></span> 
  
<span data-ttu-id="12438-464">Unter [kanonische Eigenschaft PidTagRpcOverHttpProxyAuthScheme](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) finden Sie Konstantendefinitionen, die zum Festlegen der Eigenschaft verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12438-464">See the [PidTagRpcOverHttpProxyAuthScheme Canonical Property](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) topic for constant definitions used to set the property.</span></span> 
  
### <a name="identifiers"></a><span data-ttu-id="12438-465">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="12438-465">Identifiers</span></span>

<span data-ttu-id="12438-466">Verwenden Sie das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef.h definierte `DEFINE_OLEGUID`-Makro, um die folgenden symbolischen GUID-Namen (Globally Unique Identifier) Ihren Werten zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="12438-466">Use the  `DEFINE_OLEGUID` macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the following GUID symbolic names with their values.</span></span> 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

<span data-ttu-id="12438-467">Der folgende Bezeichner gilt für den Abschnitt Capone-Profil eines Adressbuchs, der zur Unterstützung mehrerer ([MultiEx](using-multiple-exchange-accounts.md))-Postfächer eine [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)-Eigenschaft enthält, die effektiv den von [SetDefaultDir](iaddrbook-setdefaultdir.md) angegebenen standardmäßigen Container deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="12438-467">The following Identifier is for the Capone Profile section of an Address Book, which in support of multiple Exchange ([MultiEx](using-multiple-exchange-accounts.md)) mailboxes contains a [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property that effectively turns off the default container specified by [SetDefaultDir](iaddrbook-setdefaultdir.md).</span></span>
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a><span data-ttu-id="12438-468">Schnittstellenbezeichner</span><span class="sxs-lookup"><span data-stu-id="12438-468">Interface identifiers</span></span>

#### <a name="imapisync"></a><span data-ttu-id="12438-469">IMAPISync</span><span class="sxs-lookup"><span data-stu-id="12438-469">IMAPISync</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a><span data-ttu-id="12438-470">IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="12438-470">IMAPISyncProgressCallback</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iid_icontabadmin"></a><span data-ttu-id="12438-471">IID_IContabAdmin</span><span class="sxs-lookup"><span data-stu-id="12438-471">IID_IContabAdmin</span></span>
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iid_imapisecuremessage"></a><span data-ttu-id="12438-472">IID_IMAPISECUREMESSAGE</span><span class="sxs-lookup"><span data-stu-id="12438-472">IID_IMAPISECUREMESSAGE</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iid_imapigetsession"></a><span data-ttu-id="12438-473">IID_IMAPIGetSession</span><span class="sxs-lookup"><span data-stu-id="12438-473">IID_IMAPIGetSession</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a><span data-ttu-id="12438-474">Schnittstellenbezeichner für PST-Override-Handler</span><span class="sxs-lookup"><span data-stu-id="12438-474">PST Override Handler interface identifiers</span></span>

#### <a name="iid_ipstoverridereq"></a><span data-ttu-id="12438-475">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="12438-475">IID_IPSTOVERRIDEREQ</span></span>
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iid_ipstoverride1"></a><span data-ttu-id="12438-476">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="12438-476">IID_IPSTOVERRIDE1</span></span>
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a><span data-ttu-id="12438-477">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12438-477">See also</span></span>

- [<span data-ttu-id="12438-478">Informationen zu MAPI-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="12438-478">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="12438-479">Informationen zu benannten Eigenschaften in Outlook</span><span class="sxs-lookup"><span data-stu-id="12438-479">About Named Properties Used by Outlook</span></span>](about-named-properties-used-by-outlook.md)
- [<span data-ttu-id="12438-480">Zugreifen auf einen Speicher auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="12438-480">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="12438-481">Öffnen eines Speichers auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="12438-481">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="12438-482">Verwalten einer Nachricht in einem OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus</span><span class="sxs-lookup"><span data-stu-id="12438-482">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

