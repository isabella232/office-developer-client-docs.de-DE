---
title: MAPI-Konstanten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8fa5ac8d-3f63-499c-bb4e-439984773e4a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4f84ed318fa53877acd9d4759b81c140d2b32e6b
ms.sourcegitcommit: 6a8c758e690c4b7f3ab6d40635606efd31a3cc07
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2018
ms.locfileid: "25361485"
---
# <a name="mapi-constants"></a><span data-ttu-id="3709b-103">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3709b-103">MAPI constants</span></span>

<span data-ttu-id="3709b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3709b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3709b-105">Dieses Thema enthält Konstantendefinitionen, MAPI-Schnittstellendeklarationen und -Klasse und Schnittstelle Bezeichner, die von der MAPI-APIs verwendet.</span><span class="sxs-lookup"><span data-stu-id="3709b-105">This topic contains constant definitions, MAPI interface declarations, and class and interface identifiers used by the MAPI APIs.</span></span>
  
## <a name="class-and-interface-identifiers"></a><span data-ttu-id="3709b-106">Bezeichner-Klasse und Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3709b-106">Class and interface identifiers</span></span>

<span data-ttu-id="3709b-107">Verwenden Sie das DEFINE_GUID-Makro in der Microsoft Windows Software Development Kit (SDK)-Header-Datei guiddef.h definiert, deren Werte symbolische Namen global eindeutigen Bezeichner (GUID) zugeordnet, sofern nichts anderes angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3709b-107">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values, unless otherwise indicated.</span></span>
  
## <a name="attachment-security-conversion-api"></a><span data-ttu-id="3709b-108">Anlage Sicherheit Konvertierung API</span><span class="sxs-lookup"><span data-stu-id="3709b-108">Attachment security conversion API</span></span>

<span data-ttu-id="3709b-109">Dieser Abschnitt enthält Konstantendefinitionen und Schnittstellenbezeichner für die Anlage Security-API.</span><span class="sxs-lookup"><span data-stu-id="3709b-109">This section contains constant definitions and interface identifiers for the Attachment Security API.</span></span>
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

<span data-ttu-id="3709b-110">Verwenden Sie das MAPIMETHOD Makro in der Windows SDK-Header-Datei mapidefs.h definiert, um die reinen virtuellen Funktion **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)** definieren.</span><span class="sxs-lookup"><span data-stu-id="3709b-110">Use the MAPIMETHOD macro defined in the Windows SDK header file mapidefs.h to define the pure virtual function **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)**.</span></span> 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

<span data-ttu-id="3709b-111">Verwenden Sie DECLARE_MAPI_INTERFACE_ Makros in der Windows SDK-Header-Datei mapidefs.h definiert, um die Tabelle virtueller Methoden für **["IAttachmentSecurity"](iattachmentsecurityiunknown.md)** definieren.</span><span class="sxs-lookup"><span data-stu-id="3709b-111">Use the DECLARE_MAPI_INTERFACE_ macro defined in the Windows SDK header file mapidefs.h to define the virtual method table for **[IAttachmentSecurity](iattachmentsecurityiunknown.md)**.</span></span> 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a><span data-ttu-id="3709b-112">MAPI-MIME-Konvertierung API</span><span class="sxs-lookup"><span data-stu-id="3709b-112">MAPI-MIME conversion API</span></span>

<span data-ttu-id="3709b-113">Dieser Abschnitt enthält Konstantendefinitionen und -Klasse und Schnittstelle Bezeichner für die MAPI-MIME-Konvertierung-API.</span><span class="sxs-lookup"><span data-stu-id="3709b-113">This section contains constant definitions and class and interface identifiers for the MAPI-MIME Conversion API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="3709b-114">Konstanten</span><span class="sxs-lookup"><span data-stu-id="3709b-114">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3709b-115">CCSF_SMTP</span><span class="sxs-lookup"><span data-stu-id="3709b-115">CCSF_SMTP</span></span>  <br/> |<span data-ttu-id="3709b-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="3709b-116">0x0002</span></span>  <br/> |
|<span data-ttu-id="3709b-117">CCSF_NOHEADERS</span><span class="sxs-lookup"><span data-stu-id="3709b-117">CCSF_NOHEADERS</span></span>  <br/> |<span data-ttu-id="3709b-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="3709b-118">0x0004</span></span>  <br/> |
|<span data-ttu-id="3709b-119">CCSF_USE_TNEF</span><span class="sxs-lookup"><span data-stu-id="3709b-119">CCSF_USE_TNEF</span></span>  <br/> | <span data-ttu-id="3709b-120">0x0010</span><span class="sxs-lookup"><span data-stu-id="3709b-120">0x0010</span></span>  <br/> |
|<span data-ttu-id="3709b-121">CCSF_INCLUDE_BCC</span><span class="sxs-lookup"><span data-stu-id="3709b-121">CCSF_INCLUDE_BCC</span></span>  <br/> |<span data-ttu-id="3709b-122">0 x 0020</span><span class="sxs-lookup"><span data-stu-id="3709b-122">0x0020</span></span>  <br/> |
|<span data-ttu-id="3709b-123">CCSF_8BITHEADERS</span><span class="sxs-lookup"><span data-stu-id="3709b-123">CCSF_8BITHEADERS</span></span>  <br/> | <span data-ttu-id="3709b-124">0x0040</span><span class="sxs-lookup"><span data-stu-id="3709b-124">0x0040</span></span>  <br/> |
|<span data-ttu-id="3709b-125">CCSF_USE_RTF</span><span class="sxs-lookup"><span data-stu-id="3709b-125">CCSF_USE_RTF</span></span>  <br/> |<span data-ttu-id="3709b-126">0 x 0080</span><span class="sxs-lookup"><span data-stu-id="3709b-126">0x0080</span></span>  <br/> |
|<span data-ttu-id="3709b-127">CCSF_PLAIN_TEXT_ONLY</span><span class="sxs-lookup"><span data-stu-id="3709b-127">CCSF_PLAIN_TEXT_ONLY</span></span>  <br/> |<span data-ttu-id="3709b-128">0 x 1000</span><span class="sxs-lookup"><span data-stu-id="3709b-128">0x1000</span></span>  <br/> |
|<span data-ttu-id="3709b-129">CCSF_NO_MSGID</span><span class="sxs-lookup"><span data-stu-id="3709b-129">CCSF_NO_MSGID</span></span>  <br/> |<span data-ttu-id="3709b-130">0 x 4000</span><span class="sxs-lookup"><span data-stu-id="3709b-130">0x4000</span></span>  <br/> |
|<span data-ttu-id="3709b-131">CCSF_GLOBAL_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="3709b-131">CCSF_GLOBAL_MESSAGE</span></span>  <br/> |<span data-ttu-id="3709b-132">0x00200000</span><span class="sxs-lookup"><span data-stu-id="3709b-132">0x00200000</span></span>  <br/> |
|<span data-ttu-id="3709b-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3709b-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="3709b-134">*Wie in der Microsoft Windows Software Development Kit (SDK) Headerdatei winerror.h definiert*</span><span class="sxs-lookup"><span data-stu-id="3709b-134">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="3709b-135">Class Identifier</span><span class="sxs-lookup"><span data-stu-id="3709b-135">Class identifiers</span></span>

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a><span data-ttu-id="3709b-136">Schnittstelle-IDs</span><span class="sxs-lookup"><span data-stu-id="3709b-136">Interface identifiers</span></span>

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a><span data-ttu-id="3709b-137">Offline-Status-API</span><span class="sxs-lookup"><span data-stu-id="3709b-137">Offline State API</span></span>

<span data-ttu-id="3709b-138">Dieser Abschnitt enthält Konstantendefinitionen und -Klasse und Schnittstelle Bezeichner für Zustand-API.</span><span class="sxs-lookup"><span data-stu-id="3709b-138">This section contains constant definitions and class and interface identifiers for the Offline State API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="3709b-139">Konstanten</span><span class="sxs-lookup"><span data-stu-id="3709b-139">Constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3709b-140">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3709b-140">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="3709b-141">*Wie in der Microsoft Windows Software Development Kit (SDK) Headerdatei winerror.h definiert*</span><span class="sxs-lookup"><span data-stu-id="3709b-141">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="3709b-142">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="3709b-142">E_NOINTERFACE</span></span>  <br/> | <span data-ttu-id="3709b-143">*Gemäß Definition in der Headerdatei winerror.h Windows (SDK)*</span><span class="sxs-lookup"><span data-stu-id="3709b-143">*As defined in the Windows (SDK) header file winerror.h*</span></span>  <br/> |
|<span data-ttu-id="3709b-144">MAPIOFFLINE_ADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="3709b-144">MAPIOFFLINE_ADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="3709b-145">(ULONG) 0</span><span class="sxs-lookup"><span data-stu-id="3709b-145">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="3709b-146">MAPIOFFLINE_UNADVISE_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="3709b-146">MAPIOFFLINE_UNADVISE_DEFAULT</span></span>  <br/> |<span data-ttu-id="3709b-147">(ULONG) 0</span><span class="sxs-lookup"><span data-stu-id="3709b-147">(ULONG)0</span></span>  <br/> |
|<span data-ttu-id="3709b-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="3709b-148">MAPIOFFLINE_ADVISE_TYPE_STATECHANGE</span></span>  <br/> |<span data-ttu-id="3709b-149">1</span><span class="sxs-lookup"><span data-stu-id="3709b-149">1</span></span>  <br/> |
|<span data-ttu-id="3709b-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="3709b-150">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="3709b-151">0 x 1</span><span class="sxs-lookup"><span data-stu-id="3709b-151">0x1</span></span>  <br/> |
|<span data-ttu-id="3709b-152">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="3709b-152">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="3709b-153">0 x 2</span><span class="sxs-lookup"><span data-stu-id="3709b-153">0x2</span></span>  <br/> |
|<span data-ttu-id="3709b-154">MAPIOFFLINE_FLAG_BLOCK</span><span class="sxs-lookup"><span data-stu-id="3709b-154">MAPIOFFLINE_FLAG_BLOCK</span></span>  <br/> |<span data-ttu-id="3709b-155">0 x 00002000</span><span class="sxs-lookup"><span data-stu-id="3709b-155">0x00002000</span></span>  <br/> |
|<span data-ttu-id="3709b-156">MAPIOFFLINE_FLAG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="3709b-156">MAPIOFFLINE_FLAG_DEFAULT</span></span>  <br/> |<span data-ttu-id="3709b-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3709b-157">0x00000000</span></span>  <br/> |
|<span data-ttu-id="3709b-158">MAPIOFFLINE_STATE_ALL</span><span class="sxs-lookup"><span data-stu-id="3709b-158">MAPIOFFLINE_STATE_ALL</span></span>  <br/> |<span data-ttu-id="3709b-159">0x003f037f</span><span class="sxs-lookup"><span data-stu-id="3709b-159">0x003f037f</span></span>  <br/> |
|<span data-ttu-id="3709b-160">**Online oder offline**</span><span class="sxs-lookup"><span data-stu-id="3709b-160">**Online or offline**</span></span> <br/> ||
|<span data-ttu-id="3709b-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span><span class="sxs-lookup"><span data-stu-id="3709b-161">MAPIOFFLINE_STATE_OFFLINE_MASK</span></span>  <br/> |<span data-ttu-id="3709b-162">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="3709b-162">0x00000003</span></span>  <br/> |
|<span data-ttu-id="3709b-163">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="3709b-163">MAPIOFFLINE_STATE_OFFLINE</span></span>  <br/> |<span data-ttu-id="3709b-164">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3709b-164">0x00000001</span></span>  <br/> |
|<span data-ttu-id="3709b-165">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="3709b-165">MAPIOFFLINE_STATE_ONLINE</span></span>  <br/> |<span data-ttu-id="3709b-166">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3709b-166">0x00000002</span></span>  <br/> |
   
### <a name="class-identifiers"></a><span data-ttu-id="3709b-167">Class Identifier</span><span class="sxs-lookup"><span data-stu-id="3709b-167">Class identifiers</span></span>

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a><span data-ttu-id="3709b-168">Schnittstelle-IDs</span><span class="sxs-lookup"><span data-stu-id="3709b-168">Interface identifiers</span></span>

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

## <a name="outlook-named-properties"></a><span data-ttu-id="3709b-169">Benannte Eigenschaften Outlook</span><span class="sxs-lookup"><span data-stu-id="3709b-169">Outlook named properties</span></span>

<span data-ttu-id="3709b-170">Dieser Abschnitt enthält Konstantendefinitionen für benannte Eigenschaften und deren Namespaces und andere zugehörigen-Konstanten.</span><span class="sxs-lookup"><span data-stu-id="3709b-170">This section contains constant definitions for named properties and their namespaces, and other related constants.</span></span>
  
### <a name="definitions-for-named-properties"></a><span data-ttu-id="3709b-171">Definitionen für benannte Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3709b-171">Definitions for named properties</span></span>

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

### <a name="definitions-for-namespaces"></a><span data-ttu-id="3709b-172">Definitionen für namespaces</span><span class="sxs-lookup"><span data-stu-id="3709b-172">Definitions for namespaces</span></span>

<span data-ttu-id="3709b-173">Die folgenden global eindeutigen Bezeichner (GUIDs) repräsentieren die Namespaces der benannten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3709b-173">The following globally unique identifiers (GUIDs) represent the namespaces of the named properties.</span></span>
  
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

<span data-ttu-id="3709b-174">Finden Sie im Abschnitt MAPI-Speicher für die PSETID-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="3709b-174">Refer to the section MAPI Store for the PSETID definitions.</span></span>
  
### <a name="other-constants"></a><span data-ttu-id="3709b-175">Anderen-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3709b-175">Other constants</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3709b-176">INSP_ONEOFFFLAGS</span><span class="sxs-lookup"><span data-stu-id="3709b-176">INSP_ONEOFFFLAGS</span></span>  <br/> |<span data-ttu-id="3709b-177">0xD000000</span><span class="sxs-lookup"><span data-stu-id="3709b-177">0xD000000</span></span>  <br/> |
|<span data-ttu-id="3709b-178">INSP_PROPDEFINITION</span><span class="sxs-lookup"><span data-stu-id="3709b-178">INSP_PROPDEFINITION</span></span>  <br/> |<span data-ttu-id="3709b-179">0x2000000</span><span class="sxs-lookup"><span data-stu-id="3709b-179">0x2000000</span></span>  <br/> |
|<span data-ttu-id="3709b-180">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="3709b-180">MNID_ID</span></span>  <br/> | <span data-ttu-id="3709b-181">*Wie in der Header-Datei mapidefs.h definiert.*</span><span class="sxs-lookup"><span data-stu-id="3709b-181">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="3709b-182">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="3709b-182">MNID_STRING</span></span>  <br/> | <span data-ttu-id="3709b-183">*Wie in der Header-Datei mapidefs.h definiert.*</span><span class="sxs-lookup"><span data-stu-id="3709b-183">*As defined in the header file mapidefs.h.*</span></span>  <br/> |
|<span data-ttu-id="3709b-184">mtgNone</span><span class="sxs-lookup"><span data-stu-id="3709b-184">mtgNone</span></span>  <br/> |<span data-ttu-id="3709b-185">0 x 0</span><span class="sxs-lookup"><span data-stu-id="3709b-185">0x0</span></span>  <br/> |
|<span data-ttu-id="3709b-186">mtgRequest</span><span class="sxs-lookup"><span data-stu-id="3709b-186">mtgRequest</span></span>  <br/> |<span data-ttu-id="3709b-187">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3709b-187">0x00000001</span></span>  <br/> |
|<span data-ttu-id="3709b-188">mtgFullUpdate</span><span class="sxs-lookup"><span data-stu-id="3709b-188">mtgFullUpdate</span></span>  <br/> |<span data-ttu-id="3709b-189">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="3709b-189">0x00010000</span></span>  <br/> |
|<span data-ttu-id="3709b-190">mtgInfoUpdate</span><span class="sxs-lookup"><span data-stu-id="3709b-190">mtgInfoUpdate</span></span>  <br/> |<span data-ttu-id="3709b-191">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="3709b-191">0x00020000</span></span>  <br/> |
|<span data-ttu-id="3709b-192">mtgOutofDate</span><span class="sxs-lookup"><span data-stu-id="3709b-192">mtgOutofDate</span></span>  <br/> |<span data-ttu-id="3709b-193">0x00080000</span><span class="sxs-lookup"><span data-stu-id="3709b-193">0x00080000</span></span>  <br/> |
|<span data-ttu-id="3709b-194">mtgDelegated</span><span class="sxs-lookup"><span data-stu-id="3709b-194">mtgDelegated</span></span>  <br/> |<span data-ttu-id="3709b-195">0x00100000</span><span class="sxs-lookup"><span data-stu-id="3709b-195">0x00100000</span></span>  <br/> |
   
## <a name="replication-api"></a><span data-ttu-id="3709b-196">Replikations-API</span><span class="sxs-lookup"><span data-stu-id="3709b-196">Replication API</span></span>

<span data-ttu-id="3709b-197">Dieser Abschnitt enthält Konstantendefinitionen, MAPI-Schnittstellendeklarationen und -Klasse und Schnittstelle Bezeichner für die Replikation-API.</span><span class="sxs-lookup"><span data-stu-id="3709b-197">This section contains constant definitions, MAPI interface declarations, and class and interface identifiers for the Replication API.</span></span>
  
### <a name="constants"></a><span data-ttu-id="3709b-198">Konstanten</span><span class="sxs-lookup"><span data-stu-id="3709b-198">Constants</span></span>

<span data-ttu-id="3709b-199">Es folgt eine [MAPIUID](mapiuid.md) -Struktur, die einen MAPI-Dienstanbieter identifiziert:</span><span class="sxs-lookup"><span data-stu-id="3709b-199">The following is a [MAPIUID](mapiuid.md) structure identifying a MAPI service provider:</span></span> 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|<span data-ttu-id="3709b-200">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="3709b-200">DNH_OK</span></span>  <br/> |<span data-ttu-id="3709b-201">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="3709b-201">0x00010000</span></span>  <br/> |
|<span data-ttu-id="3709b-202">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="3709b-202">DNT_OK</span></span>  <br/> |<span data-ttu-id="3709b-203">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="3709b-203">0x00010000</span></span>  <br/> |
|<span data-ttu-id="3709b-204">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="3709b-204">HSF_LOCAL</span></span>  <br/> |<span data-ttu-id="3709b-205">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="3709b-205">0x00000008</span></span>  <br/> |
|<span data-ttu-id="3709b-206">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="3709b-206">HSF_COPYDESTRUCTIVE</span></span>  <br/> |<span data-ttu-id="3709b-207">0 x 00000010</span><span class="sxs-lookup"><span data-stu-id="3709b-207">0x00000010</span></span>  <br/> |
|<span data-ttu-id="3709b-208">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="3709b-208">HSF_OK</span></span>  <br/> |<span data-ttu-id="3709b-209">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="3709b-209">0x00010000</span></span>  <br/> |
|<span data-ttu-id="3709b-210">MDB_OST_LOGON_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3709b-210">MDB_OST_LOGON_UNICODE</span></span>  <br/> |<span data-ttu-id="3709b-211">((ULONG) 0X00000800)</span><span class="sxs-lookup"><span data-stu-id="3709b-211">((ULONG) 0x00000800)</span></span>  <br/> |
|<span data-ttu-id="3709b-212">MDB_OST_LOGON_ANSI</span><span class="sxs-lookup"><span data-stu-id="3709b-212">MDB_OST_LOGON_ANSI</span></span>  <br/> |<span data-ttu-id="3709b-213">((ULONG) 0 X 00001000)</span><span class="sxs-lookup"><span data-stu-id="3709b-213">((ULONG) 0x00001000)</span></span>  <br/> |
|<span data-ttu-id="3709b-214">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="3709b-214">SHOW_SOFT_DELETES</span></span>  <br/> |<span data-ttu-id="3709b-215">((ULONG) 0 X 00000002)</span><span class="sxs-lookup"><span data-stu-id="3709b-215">((ULONG) 0x00000002)</span></span>  <br/> |
|<span data-ttu-id="3709b-216">SS_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="3709b-216">SS_ACTIVE</span></span>  <br/> |<span data-ttu-id="3709b-217">0</span><span class="sxs-lookup"><span data-stu-id="3709b-217">0</span></span>  <br/> |
|<span data-ttu-id="3709b-218">SS_SUSPENDED</span><span class="sxs-lookup"><span data-stu-id="3709b-218">SS_SUSPENDED</span></span>  <br/> |<span data-ttu-id="3709b-219">1</span><span class="sxs-lookup"><span data-stu-id="3709b-219">1</span></span>  <br/> |
|<span data-ttu-id="3709b-220">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="3709b-220">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="3709b-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3709b-221">0x00000001</span></span>  <br/> |
|<span data-ttu-id="3709b-222">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="3709b-222">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="3709b-223">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3709b-223">0x00000002</span></span>  <br/> |
|<span data-ttu-id="3709b-224">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="3709b-224">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="3709b-225">0 x 00000040</span><span class="sxs-lookup"><span data-stu-id="3709b-225">0x00000040</span></span>  <br/> |
|<span data-ttu-id="3709b-226">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="3709b-226">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="3709b-227">0x00000080</span><span class="sxs-lookup"><span data-stu-id="3709b-227">0x00000080</span></span>  <br/> |
|<span data-ttu-id="3709b-228">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="3709b-228">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="3709b-229">0 x 00000200</span><span class="sxs-lookup"><span data-stu-id="3709b-229">0x00000200</span></span>  <br/> |
|<span data-ttu-id="3709b-230">SYNC_BACKGROUND</span><span class="sxs-lookup"><span data-stu-id="3709b-230">SYNC_BACKGROUND</span></span>  <br/> |<span data-ttu-id="3709b-231">0 x 00001000</span><span class="sxs-lookup"><span data-stu-id="3709b-231">0x00001000</span></span>  <br/> |
|<span data-ttu-id="3709b-232">SYNC_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="3709b-232">SYNC_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="3709b-233">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="3709b-233">0x00020000</span></span>  <br/> |
|<span data-ttu-id="3709b-234">SYNC_HEADERS</span><span class="sxs-lookup"><span data-stu-id="3709b-234">SYNC_HEADERS</span></span>  <br/> |<span data-ttu-id="3709b-235">0x02000000</span><span class="sxs-lookup"><span data-stu-id="3709b-235">0x02000000</span></span>  <br/> |
|<span data-ttu-id="3709b-236">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="3709b-236">UPC_OK</span></span>  <br/> |<span data-ttu-id="3709b-237">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="3709b-237">0x00010000</span></span>  <br/> |
|<span data-ttu-id="3709b-238">UPD_ASSOC</span><span class="sxs-lookup"><span data-stu-id="3709b-238">UPD_ASSOC</span></span>  <br/> |<span data-ttu-id="3709b-239">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3709b-239">0x00000001</span></span>  <br/> |
|<span data-ttu-id="3709b-240">UPD_MOV</span><span class="sxs-lookup"><span data-stu-id="3709b-240">UPD_MOV</span></span>  <br/> |<span data-ttu-id="3709b-241">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3709b-241">0x00000002</span></span>  <br/> |
|<span data-ttu-id="3709b-242">UPD_OK</span><span class="sxs-lookup"><span data-stu-id="3709b-242">UPD_OK</span></span>  <br/> |<span data-ttu-id="3709b-243">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="3709b-243">0x00010000</span></span>  <br/> |
|<span data-ttu-id="3709b-244">UPD_MOVED</span><span class="sxs-lookup"><span data-stu-id="3709b-244">UPD_MOVED</span></span>  <br/> |<span data-ttu-id="3709b-245">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="3709b-245">0x00020000</span></span>  <br/> |
|<span data-ttu-id="3709b-246">UPD_UPDATE</span><span class="sxs-lookup"><span data-stu-id="3709b-246">UPD_UPDATE</span></span>  <br/> |<span data-ttu-id="3709b-247">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="3709b-247">0x00040000</span></span>  <br/> |
|<span data-ttu-id="3709b-248">UPD_COMMIT</span><span class="sxs-lookup"><span data-stu-id="3709b-248">UPD_COMMIT</span></span>  <br/> |<span data-ttu-id="3709b-249">0x00080000</span><span class="sxs-lookup"><span data-stu-id="3709b-249">0x00080000</span></span>  <br/> |
|<span data-ttu-id="3709b-250">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="3709b-250">UPF_NEW</span></span>  <br/> |<span data-ttu-id="3709b-251">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3709b-251">0x00000001</span></span>  <br/> |
|<span data-ttu-id="3709b-252">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="3709b-252">UPF_MOD_PARENT</span></span>  <br/> |<span data-ttu-id="3709b-253">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3709b-253">0x00000002</span></span>  <br/> |
|<span data-ttu-id="3709b-254">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="3709b-254">UPF_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="3709b-255">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="3709b-255">0x00000004</span></span>  <br/> |
|<span data-ttu-id="3709b-256">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="3709b-256">UPF_DEL</span></span>  <br/> |<span data-ttu-id="3709b-257">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="3709b-257">0x00000008</span></span>  <br/> |
|<span data-ttu-id="3709b-258">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="3709b-258">UPF_OK</span></span>  <br/> |<span data-ttu-id="3709b-259">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="3709b-259">0x00010000</span></span>  <br/> |
|<span data-ttu-id="3709b-260">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="3709b-260">UPH_OK</span></span>  <br/> |<span data-ttu-id="3709b-261">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="3709b-261">0x00010000</span></span>  <br/> |
|<span data-ttu-id="3709b-262">UPM_ASSOC</span><span class="sxs-lookup"><span data-stu-id="3709b-262">UPM_ASSOC</span></span>  <br/> |<span data-ttu-id="3709b-263">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3709b-263">0x00000001</span></span>  <br/> |
|<span data-ttu-id="3709b-264">UPM_NEW</span><span class="sxs-lookup"><span data-stu-id="3709b-264">UPM_NEW</span></span>  <br/> |<span data-ttu-id="3709b-265">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3709b-265">0x00000002</span></span>  <br/> |
|<span data-ttu-id="3709b-266">UPM_MOV</span><span class="sxs-lookup"><span data-stu-id="3709b-266">UPM_MOV</span></span>  <br/> |<span data-ttu-id="3709b-267">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="3709b-267">0x00000004</span></span>  <br/> |
|<span data-ttu-id="3709b-268">UPM_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="3709b-268">UPM_MOD_PROPS</span></span>  <br/> |<span data-ttu-id="3709b-269">0 x 00000008</span><span class="sxs-lookup"><span data-stu-id="3709b-269">0x00000008</span></span>  <br/> |
|<span data-ttu-id="3709b-270">UPM_HEADER</span><span class="sxs-lookup"><span data-stu-id="3709b-270">UPM_HEADER</span></span>  <br/> |<span data-ttu-id="3709b-271">0 x 00000010</span><span class="sxs-lookup"><span data-stu-id="3709b-271">0x00000010</span></span>  <br/> |
|<span data-ttu-id="3709b-272">UPM_OK</span><span class="sxs-lookup"><span data-stu-id="3709b-272">UPM_OK</span></span>  <br/> |<span data-ttu-id="3709b-273">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="3709b-273">0x00010000</span></span>  <br/> |
|<span data-ttu-id="3709b-274">UPM_MOVED</span><span class="sxs-lookup"><span data-stu-id="3709b-274">UPM_MOVED</span></span>  <br/> |<span data-ttu-id="3709b-275">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="3709b-275">0x00020000</span></span>  <br/> |
|<span data-ttu-id="3709b-276">UPM_COMMIT</span><span class="sxs-lookup"><span data-stu-id="3709b-276">UPM_COMMIT</span></span>  <br/> |<span data-ttu-id="3709b-277">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="3709b-277">0x00040000</span></span>  <br/> |
|<span data-ttu-id="3709b-278">UPM_DELETE</span><span class="sxs-lookup"><span data-stu-id="3709b-278">UPM_DELETE</span></span>  <br/> |<span data-ttu-id="3709b-279">0x00080000</span><span class="sxs-lookup"><span data-stu-id="3709b-279">0x00080000</span></span>  <br/> |
|<span data-ttu-id="3709b-280">UPM_SAVE</span><span class="sxs-lookup"><span data-stu-id="3709b-280">UPM_SAVE</span></span>  <br/> |<span data-ttu-id="3709b-281">0x00100000</span><span class="sxs-lookup"><span data-stu-id="3709b-281">0x00100000</span></span>  <br/> |
|<span data-ttu-id="3709b-282">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="3709b-282">UPR_ASSOC</span></span>  <br/> |<span data-ttu-id="3709b-283">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3709b-283">0x00000001</span></span>  <br/> |
|<span data-ttu-id="3709b-284">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="3709b-284">UPR_READ</span></span>  <br/> |<span data-ttu-id="3709b-285">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3709b-285">0x00000002</span></span>  <br/> |
|<span data-ttu-id="3709b-286">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="3709b-286">UPR_OK</span></span>  <br/> |<span data-ttu-id="3709b-287">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="3709b-287">0x00010000</span></span>  <br/> |
|<span data-ttu-id="3709b-288">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="3709b-288">UPR_COMMIT</span></span>  <br/> |<span data-ttu-id="3709b-289">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="3709b-289">0x00020000</span></span>  <br/> |
|<span data-ttu-id="3709b-290">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="3709b-290">UPS_UPLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="3709b-291">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3709b-291">0x00000001</span></span>  <br/> |
|<span data-ttu-id="3709b-292">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="3709b-292">UPS_DNLOAD_ONLY</span></span>  <br/> |<span data-ttu-id="3709b-293">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3709b-293">0x00000002</span></span>  <br/> |
|<span data-ttu-id="3709b-294">UPS_ONE_FOLDER</span><span class="sxs-lookup"><span data-stu-id="3709b-294">UPS_ONE_FOLDER</span></span>  <br/> |<span data-ttu-id="3709b-295">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="3709b-295">0x00000004</span></span>  <br/> |
|<span data-ttu-id="3709b-296">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="3709b-296">UPS_THESE_FOLDERS</span></span>  <br/> |<span data-ttu-id="3709b-297">0x00000080</span><span class="sxs-lookup"><span data-stu-id="3709b-297">0x00000080</span></span>  <br/> |
|<span data-ttu-id="3709b-298">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="3709b-298">UPS_OK</span></span>  <br/> |<span data-ttu-id="3709b-299">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="3709b-299">0x00010000</span></span>  <br/> |
|<span data-ttu-id="3709b-300">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="3709b-300">UPT_OK</span></span>  <br/> |<span data-ttu-id="3709b-301">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="3709b-301">0x00010000</span></span>  <br/> |
|<span data-ttu-id="3709b-302">UPT_PUBLIC</span><span class="sxs-lookup"><span data-stu-id="3709b-302">UPT_PUBLIC</span></span>  <br/> |<span data-ttu-id="3709b-303">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3709b-303">0x00000001</span></span>  <br/> |
|<span data-ttu-id="3709b-304">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="3709b-304">UPV_ERROR</span></span>  <br/> |<span data-ttu-id="3709b-305">0 x 00010000</span><span class="sxs-lookup"><span data-stu-id="3709b-305">0x00010000</span></span>  <br/> |
|<span data-ttu-id="3709b-306">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="3709b-306">UPV_DIRTY</span></span>  <br/> |<span data-ttu-id="3709b-307">0 x 00020000</span><span class="sxs-lookup"><span data-stu-id="3709b-307">0x00020000</span></span>  <br/> |
|<span data-ttu-id="3709b-308">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="3709b-308">UPV_COMMIT</span></span>  <br/> |<span data-ttu-id="3709b-309">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="3709b-309">0x00040000</span></span>  <br/> |
   
### <a name="interface-declarations"></a><span data-ttu-id="3709b-310">Schnittstellendeklarationen</span><span class="sxs-lookup"><span data-stu-id="3709b-310">Interface declarations</span></span>

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a><span data-ttu-id="3709b-311">Schnittstelle-IDs</span><span class="sxs-lookup"><span data-stu-id="3709b-311">Interface identifiers</span></span>

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

<span data-ttu-id="3709b-312">Verwenden Sie die folgende Schnittstellenbezeichner mit [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md)oder [IMsgStore::OpenEntry](imsgstore-openentry.md) öffnen und alle Kontrollkästchen Anbieter auf ein Folder-Objekt und ein Meldungsobjekt jeweils ignorieren.</span><span class="sxs-lookup"><span data-stu-id="3709b-312">Use the two following interface identifiers with [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), or [IMsgStore::OpenEntry](imsgstore-openentry.md) to open and ignore any provider check on a folder object and a message object, respectively.</span></span> 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a><span data-ttu-id="3709b-313">MAPI-Speicher</span><span class="sxs-lookup"><span data-stu-id="3709b-313">MAPI store</span></span>

<span data-ttu-id="3709b-314">Dieser Abschnitt enthält Konstantendefinitionen und Schnittstellenbezeichner vom verwendet APIs Schnittstelle mit einem MAPI-Speicher.</span><span class="sxs-lookup"><span data-stu-id="3709b-314">This section contains constant definitions and interface identifiers used by APIs that interface with a MAPI store.</span></span>
  
### <a name="constants"></a><span data-ttu-id="3709b-315">Konstanten</span><span class="sxs-lookup"><span data-stu-id="3709b-315">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="3709b-316">fnevIndexing</span><span class="sxs-lookup"><span data-stu-id="3709b-316">fnevIndexing</span></span>  <br/> |<span data-ttu-id="3709b-317">((ULONG) 0 X 00010000)</span><span class="sxs-lookup"><span data-stu-id="3709b-317">((ULONG) 0x00010000)</span></span>  <br/> |<span data-ttu-id="3709b-318">Ein Anbieter anmelden kann **FnevIndexing** Geben Sie im **UlEventType** Member der Struktur **[Benachrichtigung](notification.md)** um der Indizierung zu benachrichtigen, dass ein Objekt für die Indizierung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="3709b-318">A store provider can specify **fnevIndexing** in the **ulEventType** member of the **[NOTIFICATION](notification.md)** structure to notify the indexer that an object is ready for indexing.</span></span> <span data-ttu-id="3709b-319">Der **Info** -Member der Struktur **Benachrichtigung** enthält eine **[EXTENDED_NOTIFICATION](extended_notification.md)** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3709b-319">The **info** member of the **NOTIFICATION** structure contains an **[EXTENDED_NOTIFICATION](extended_notification.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="3709b-320">FS_NONE</span><span class="sxs-lookup"><span data-stu-id="3709b-320">FS_NONE</span></span>  <br/> |<span data-ttu-id="3709b-321">0 x 00</span><span class="sxs-lookup"><span data-stu-id="3709b-321">0x00</span></span>  <br/> |<span data-ttu-id="3709b-322">Ein Client kann **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** und die Kontrollkästchen für die zurückgegebene Bitmaske aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3709b-322">A client can call **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** and check for the returned bitmask.</span></span> <span data-ttu-id="3709b-323">**FS_NONE** gibt an, dass der Ordner Freigabe nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3709b-323">**FS_NONE** indicates that the folder does not support sharing.</span></span>  <br/> |
|<span data-ttu-id="3709b-324">FS_SUPPORTS_SHARING</span><span class="sxs-lookup"><span data-stu-id="3709b-324">FS_SUPPORTS_SHARING</span></span>  <br/> |<span data-ttu-id="3709b-325">0x01</span><span class="sxs-lookup"><span data-stu-id="3709b-325">0x01</span></span>  <br/> |<span data-ttu-id="3709b-326">Ein Client kann **IFolderSupport::GetSupportMask** und die Kontrollkästchen für die zurückgegebene Bitmaske aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3709b-326">A client can call **IFolderSupport::GetSupportMask** and check for the returned bitmask.</span></span> <span data-ttu-id="3709b-327">**FS_SUPPORTS_SHARING** gibt an, dass der Ordner Freigabe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3709b-327">**FS_SUPPORTS_SHARING** indicates that the folder supports sharing.</span></span>  <br/> |
|<span data-ttu-id="3709b-328">INDEXING_SEARCH_OWNER</span><span class="sxs-lookup"><span data-stu-id="3709b-328">INDEXING_SEARCH_OWNER</span></span>  <br/> |<span data-ttu-id="3709b-329">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="3709b-329">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="3709b-330">Identifiziert den Prozess, der eine Benachrichtigung zu einem Indexer beschäftigt ist, dass ein Objekt für die Indizierung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="3709b-330">Identifies the process that is pushing a notification to an indexer that an object is ready for indexing.</span></span>  <br/> |
|<span data-ttu-id="3709b-331">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="3709b-331">MNID_ID</span></span>  <br/> |<span data-ttu-id="3709b-332">Wie in der Microsoft Windows Software Development Kit (SDK)-Header-Datei mapidefs.h definiert</span><span class="sxs-lookup"><span data-stu-id="3709b-332">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h</span></span>  <br/> |<span data-ttu-id="3709b-333">Ein Wert für das Feld **UlKind** der **[MAPINAMEID](mapinameid.md)** Struktur.</span><span class="sxs-lookup"><span data-stu-id="3709b-333">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="3709b-334">MNID_STRING</span><span class="sxs-lookup"><span data-stu-id="3709b-334">MNID_STRING</span></span>  <br/> |<span data-ttu-id="3709b-335">Wie in der Microsoft Windows Software Development Kit (SDK)-Header-Datei mapidefs.h definiert.</span><span class="sxs-lookup"><span data-stu-id="3709b-335">As defined in the Microsoft Windows Software Development Kit (SDK) header file mapidefs.h.</span></span>  <br/> |<span data-ttu-id="3709b-336">Ein Wert für das Feld **UlKind** der **[MAPINAMEID](mapinameid.md)** Struktur.</span><span class="sxs-lookup"><span data-stu-id="3709b-336">A value for the **ulKind** field of the **[MAPINAMEID](mapinameid.md)** structure.</span></span>  <br/> |
|<span data-ttu-id="3709b-337">MSCAP_RES_ANNOTATION</span><span class="sxs-lookup"><span data-stu-id="3709b-337">MSCAP_RES_ANNOTATION</span></span>  <br/> |<span data-ttu-id="3709b-338">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="3709b-338">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="3709b-339">Wenn ein Client für **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)** **MSCAP_SEL_RESTRICTION** *MscapSelector* angibt, können **GetCapabilities** dieser Wert zurück, wenn der Informationsspeicher ungültige Parameter in einer Einschränkung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3709b-339">If a client specifies **MSCAP_SEL_RESTRICTION** in  *mscapSelector*  for **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)**, **GetCapabilities** can return this value if the store ignores invalid parameters in a restriction.</span></span>  <br/> |
|<span data-ttu-id="3709b-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span><span class="sxs-lookup"><span data-stu-id="3709b-340">MSCAP_SECURE_FOLDER_HOMEPAGES</span></span>  <br/> |<span data-ttu-id="3709b-341">((ULONG) 0 X 00000020)</span><span class="sxs-lookup"><span data-stu-id="3709b-341">((ULONG) 0x00000020)</span></span>  <br/> |<span data-ttu-id="3709b-342">Wenn ein Client für **IMSCapabilities::GetCapabilities** **MSCAP_SEL_FOLDER** *MscapSelector* angibt, können **GetCapabilities** dieser Wert zurück, wenn der Informationsspeicher einen nicht standardmäßigen Speicher ist, der unterstützt von Ordnerhomepages.</span><span class="sxs-lookup"><span data-stu-id="3709b-342">If a client specifies **MSCAP_SEL_FOLDER** in  *mscapSelector*  for **IMSCapabilities::GetCapabilities**, **GetCapabilities** can return this value if the store is a non-default store that supports folder home pages.</span></span>  <br/> |
|<span data-ttu-id="3709b-343">STORE_PUSHER_OK</span><span class="sxs-lookup"><span data-stu-id="3709b-343">STORE_PUSHER_OK</span></span>  <br/> |<span data-ttu-id="3709b-344">((ULONG) 0 X 00800000)</span><span class="sxs-lookup"><span data-stu-id="3709b-344">((ULONG) 0x00800000)</span></span>  <br/> |<span data-ttu-id="3709b-345">Ein Client kann die Eigenschaft **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** bestimmen das Merkmal eines Nachrichtenspeichers abrufen.</span><span class="sxs-lookup"><span data-stu-id="3709b-345">A client can get the property **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** to determine the characteristic of a message store.</span></span> <span data-ttu-id="3709b-346">Wenn der Anbieter das Flag **STORE_PUSHER_OK** in der Bitmaske festlegt, bedeutet, dass der MAPI-Protokollhandler wird nicht durchforstet werden den Speicher und der Speicher wird zum Pushen von Änderungen durch Benachrichtigungen auf die Indizierung Nachrichten indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="3709b-346">If the store provider sets the **STORE_PUSHER_OK** flag in the bitmask, that means the MAPI Protocol Handler will not crawl the store, and the store is responsible to push any changes through notifications to the indexer to have messages indexed.</span></span>  <br/> |
   
### <a name="definitions-for-namespaces"></a><span data-ttu-id="3709b-347">Definitionen für namespaces</span><span class="sxs-lookup"><span data-stu-id="3709b-347">Definitions for namespaces</span></span>

<span data-ttu-id="3709b-348">Die folgenden global eindeutigen Bezeichner (GUIDs) repräsentieren die Namespaces der benannten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3709b-348">The following globally unique identifiers (GUIDs) represent the namespaces of named properties.</span></span> <span data-ttu-id="3709b-349">Sie sind indiziert, durch die MAPI Protocol Handler (PH) und im schreibgeschützten Modus dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="3709b-349">They are indexed by the MAPI Protocol Handler (PH), and are documented as read-only.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="3709b-350">Benannten Eigenschaften sollte nicht zum Erstellen oder Ändern von Elementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3709b-350">The named properties should not be used to create or modify items.</span></span> 
  
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

#### <a name="mnidid-properties"></a><span data-ttu-id="3709b-351">MNID_ID-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3709b-351">MNID_ID Properties</span></span>
  
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

#### <a name="mnidstring-properties"></a><span data-ttu-id="3709b-352">MNID_STRING-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3709b-352">MNID_STRING Properties</span></span>
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a><span data-ttu-id="3709b-353">Schnittstelle-IDs</span><span class="sxs-lookup"><span data-stu-id="3709b-353">Interface identifiers</span></span>

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

<span data-ttu-id="3709b-354">Verwendung der `DEFINE_OLEGUID` Makro definiert, in der Windows SDK-Header-Datei guiddef.h, dessen Wert den folgenden GUID symbolischen Name zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="3709b-354">Use the  `DEFINE_OLEGUID` macro defined in the Windows SDK header file guiddef.h to associate the following GUID symbolic name with its value.</span></span> 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a><span data-ttu-id="3709b-355">MAPI-Adressbuch-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3709b-355">MAPI Address Book constants</span></span>

<span data-ttu-id="3709b-356">Dieser Abschnitt enthält Konstantendefinitionen für das MAPI-Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="3709b-356">This section contains constant definitions for the MAPI Address Book.</span></span>
  
### <a name="constants"></a><span data-ttu-id="3709b-357">Konstanten</span><span class="sxs-lookup"><span data-stu-id="3709b-357">Constants</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="3709b-358">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="3709b-358">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="3709b-359">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="3709b-359">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="3709b-360">Der Stammordner für ein MAPI-Address Book-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3709b-360">The root folder for a MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="3709b-361">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="3709b-361">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="3709b-362">((ULONG) 0 X 00000002)</span><span class="sxs-lookup"><span data-stu-id="3709b-362">((ULONG) 0x00000002)</span></span>  <br/> |<span data-ttu-id="3709b-363">Ein Unterordner in den Stammordner des MAPI-Address Book-Objekts enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3709b-363">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="3709b-364">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="3709b-364">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="3709b-365">((ULONG) 0 X 00000003)</span><span class="sxs-lookup"><span data-stu-id="3709b-365">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="3709b-366">Ein Address Book Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3709b-366">An address book container object.</span></span>  <br/> |
|<span data-ttu-id="3709b-367">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="3709b-367">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="3709b-368">((ULONG) 0 X 00000004)</span><span class="sxs-lookup"><span data-stu-id="3709b-368">((ULONG) 0x00000004)</span></span>  <br/> |<span data-ttu-id="3709b-369">Ein messaging User-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3709b-369">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="3709b-370">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="3709b-370">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="3709b-371">((ULONG) 0 X 00000005)</span><span class="sxs-lookup"><span data-stu-id="3709b-371">((ULONG) 0x00000005)</span></span>  <br/> |<span data-ttu-id="3709b-372">Verteilung von List-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3709b-372">A distribution list object.</span></span>  <br/> |
   
## <a name="additional-mapi-constants"></a><span data-ttu-id="3709b-373">Zusätzliche MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3709b-373">Additional MAPI constants</span></span>

<span data-ttu-id="3709b-374">Dieser Abschnitt enthält Konstantendefinitionen einschließlich Fehlercodes und Schnittstelle-IDs von MAPI-APIs, die zuvor nicht verfügbar gemacht und dokumentiert wurden verwendet.</span><span class="sxs-lookup"><span data-stu-id="3709b-374">This section contains constant definitions including error codes, and interface identifiers used by MAPI APIs that were not previously exposed and documented.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="3709b-375">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="3709b-375">DIALOG_MODAL</span></span>  <br/> |<span data-ttu-id="3709b-376">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="3709b-376">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="3709b-377">Wenn ein Client die [IAddrBook::Details](iaddrbook-details.md) -Methode aufruft, muss der Client das Flag **DIALOG_MODAL** im _UlFlags_ -Parameter zum Anzeigen des modalen Dialogfelds, das die Details zu einer bestimmten Adressbuch Adresseintrag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3709b-377">When a client calls the [IAddrBook::Details](iaddrbook-details.md) method, the client must set the **DIALOG_MODAL** flag in the  _ulFlags_ parameter to display the modal dialog box showing the details about a particular address book entry.</span></span> <span data-ttu-id="3709b-378">Diese Konstante wird in mapidefs.h definiert.</span><span class="sxs-lookup"><span data-stu-id="3709b-378">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="3709b-379">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="3709b-379">ITEMPROC_FORCE</span></span>  <br/> |<span data-ttu-id="3709b-380">0x00000800</span><span class="sxs-lookup"><span data-stu-id="3709b-380">0x00000800</span></span>  <br/> |<span data-ttu-id="3709b-381">In Outlook 2007 gepackten PST-Speicher verfügen, Regeln und Spamfilterung für neue Nachrichten verarbeitet, bevor der neuen Nachrichten MAPI-Clients benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="3709b-381">In Outlook 2007, wrapped PST stores have rules and spam filtering processed on new messages before MAPI clients are notified of the new messages.</span></span> <span data-ttu-id="3709b-382">Einen Anbieter oder -Client wird mithilfe der [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode zum Erstellen einer neuen Nachricht in PST-Speicher sollte das Flag **ITEMPROC_FORCE** im _UlFlags_ -Parameter der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um die PST-Datei anzugeben festgelegt. -Speichers, den die Nachricht ist für Regeln für die Verarbeitung, bevor der Speicher jeder listening Client die Ankunft der neuen Nachricht informiert.</span><span class="sxs-lookup"><span data-stu-id="3709b-382">A provider or client using the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method to create a new message in PST stores should set the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to indicate to the PST store that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="3709b-383">Beachten Sie, dass nur solche regelverarbeitung gilt für neue Nachrichten, die auf einem Server, der nicht auf einem Microsoft Exchange Server ist erstellt werden, da Exchange Server Regeln für Nachrichten auf dem Server verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="3709b-383">Note that such rules processing only applies to new messages created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="3709b-384">Daher muss vom Anbieter oder vom Client erstellen die Meldung dieses Flag in Kombination mit **NON_EMS_XP_SAVE**, übergeben Sie gibt an, dass der Server nicht mit einem Exchange-Server ist.</span><span class="sxs-lookup"><span data-stu-id="3709b-384">Hence the provider or client creating the message must pass this flag in combination with **NON_EMS_XP_SAVE**, which indicates the server is not an Exchange server.</span></span>  <br/> |
| <span data-ttu-id="3709b-385">MAPI_BG_SESSION</span><span class="sxs-lookup"><span data-stu-id="3709b-385">MAPI_BG_SESSION</span></span>  <br/> |<span data-ttu-id="3709b-386">0x00200000</span><span class="sxs-lookup"><span data-stu-id="3709b-386">0x00200000</span></span>  <br/> |<span data-ttu-id="3709b-387">Ein Client kann die Funktion [MAPILogonEx](mapilogonex.md) aufrufen und Festlegen des Flags **MAPI_BG_SESSION** in den _FlFlags_ -Parameter, um eine Sitzung anmelden und Vorgänge im Hintergrund auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3709b-387">A client can call the [MAPILogonEx](mapilogonex.md) function, setting the **MAPI_BG_SESSION** flag in the  _flFlags_ parameter to log on to a session and carry out any operations in the background.</span></span> <span data-ttu-id="3709b-388">Ein Client will Verarbeitung in einem Hintergrundthread oder in einem gesonderten Prozess in einer Weise, die nicht störend auf den Vordergrundthread ist, sollte es im allgemeinen [MAPILogonEx](mapilogonex.md) mit dem **MAPI_BG_SESSION** -Flag aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3709b-388">In general, if a client intends to do processing on a background thread or in a separate process in a manner that is unobtrusive to the foreground thread, it should call [MAPILogonEx](mapilogonex.md) with the **MAPI_BG_SESSION** flag.</span></span> <span data-ttu-id="3709b-389">Ein Beispiel, in dem Hiermit wird, ist eine Clientanwendung, wie etwa eine indexing-Engine, öffnen eine Persönliche Ordner Datei (PST) für den Hintergrund Typ Zugriff.</span><span class="sxs-lookup"><span data-stu-id="3709b-389">An example where this is used is a client application, such as an indexing engine, opening a Personal Folders File (PST) for background type access.</span></span>  <br/> |
|<span data-ttu-id="3709b-390">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="3709b-390">MAPI_CACHE_ONLY</span></span>  <br/> |<span data-ttu-id="3709b-391">0x00004000</span><span class="sxs-lookup"><span data-stu-id="3709b-391">0x00004000</span></span>  <br/> |<span data-ttu-id="3709b-392">Ein Client kann die Methode [IAddrBook::OpenEntry](iaddrbook-openentry.md) aufrufen im Parameter _UlFlags_ ein Adresseintrags Adressbuch öffnen, und es anschließend nur aus dem Cache Zugriff auf das **MAPI_CACHE_ONLY** -Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="3709b-392">A client can call the [IAddrBook::OpenEntry](iaddrbook-openentry.md) method, setting the **MAPI_CACHE_ONLY** flag in the  _ulFlags_ parameter to open an address book entry and to access it subsequently only from the cache.</span></span> <span data-ttu-id="3709b-393">Ein Beispiel, in dem dies verwendet wird, ist eine Clientanwendung, die zum Öffnen der globalen Adressliste im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server erstellen möchte.</span><span class="sxs-lookup"><span data-stu-id="3709b-393">An example where this is used is a client application that wants to open the Global Address List in Cached Exchange mode and access an entry in that Address Book from the cache without creating traffic between the client and the server.</span></span>  <br/> |
|<span data-ttu-id="3709b-394">MAPI_DIALOG_MODELESS</span><span class="sxs-lookup"><span data-stu-id="3709b-394">MAPI_DIALOG_MODELESS</span></span>  <br/> |<span data-ttu-id="3709b-395">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="3709b-395">0x0000000C</span></span>  <br/> |<span data-ttu-id="3709b-396">Dieser Wert kann der Simple MAPI MAPISendMail-Funktion in der _UlFlags_ -Parameter, um anzugeben, dass ein nicht modales Dialogfeld, von der standardmäßige e-Mail-Anwendung angezeigt wird übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="3709b-396">This value can be passed to the Simple MAPI MAPISendMail function in the  _ulFlags_ parameter to specify that a modeless dialog box is displayed by the default mail application.</span></span> <span data-ttu-id="3709b-397">Wenn weder die MAPI_DIALOG (0 x 00000008) dieses Flag festgelegt ist, wird kein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3709b-397">If neither this flag nor MAPI_DIALOG (0x00000008) is set, no dialog box is displayed.</span></span>  <br/> |
|<span data-ttu-id="3709b-398">MAPI_NO_CACHE</span><span class="sxs-lookup"><span data-stu-id="3709b-398">MAPI_NO_CACHE</span></span>  <br/> |<span data-ttu-id="3709b-399">0 x 00000200</span><span class="sxs-lookup"><span data-stu-id="3709b-399">0x00000200</span></span>  <br/> |<span data-ttu-id="3709b-400">Wenn Microsoft Office Outlook im Exchange-Cache-Modus und ein Speicher im Cache-Modus geöffnet wurde, kann einen Client oder Dienstanbieter [IMsgStore::OpenEntry](imsgstore-openentry.md), das Flag **MAPI_NO_CACHE** in der _UlFlags_ -Parameter zum Öffnen eines Elements festgelegt anrufen oder eine Ordner auf den remote-Speicher.</span><span class="sxs-lookup"><span data-stu-id="3709b-400">If Microsoft Office Outlook is in Cached Exchange Mode and a store has been opened in cached mode, a client or service provider can call [IMsgStore::OpenEntry](imsgstore-openentry.md), setting the **MAPI_NO_CACHE** flag in the  _ulFlags_ parameter to open an item or a folder on the remote store.</span></span> <span data-ttu-id="3709b-401">Beachten Sie, wenn Sie den Nachrichtenspeicher mit dem **MDB_ONLINE** -Flag auf dem Remoteserver öffnen, haben Sie nicht das Flag **MAPI_NO_CACHE** verwenden.</span><span class="sxs-lookup"><span data-stu-id="3709b-401">Note that if you open the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span>  <br/> |
|<span data-ttu-id="3709b-402">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3709b-402">MAPI_UNICODE</span></span>  <br/> |<span data-ttu-id="3709b-403">0 x 80000000</span><span class="sxs-lookup"><span data-stu-id="3709b-403">0x80000000</span></span>  <br/> |<span data-ttu-id="3709b-404">Ein Client oder Dienstanbieter kann die Funktion [OpenIMsgOnIStg](openimsgonistg.md) anrufen **die Option MAPI_UNICODE** im _UlFlags_ -Parameter zum Erstellen von Unicode MSG-Dateien festlegen.</span><span class="sxs-lookup"><span data-stu-id="3709b-404">A client or service provider can call the [OpenIMsgOnIStg](openimsgonistg.md) function, setting the **MAPI_UNICODE** flag in the  _ulFlags_ parameter to create Unicode .msg files.</span></span> <span data-ttu-id="3709b-405">Das resultierende [IMessage: IMAPIProp](imessageimapiprop.md) Datei zeigt **STORE_UNICODE_OK** in seiner [PidTagStoreSupportMask kanonische-Eigenschaft](pidtagstoresupportmask-canonical-property.md) und unterstützt Unicode-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3709b-405">The resulting [IMessage : IMAPIProp](imessageimapiprop.md) file shows **STORE_UNICODE_OK** in its [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> <span data-ttu-id="3709b-406">Diese Konstante wird in mapidefs.h definiert.</span><span class="sxs-lookup"><span data-stu-id="3709b-406">This constant is defined in mapidefs.h.</span></span>  <br/> |
|<span data-ttu-id="3709b-407">MDB_ONLINE</span><span class="sxs-lookup"><span data-stu-id="3709b-407">MDB_ONLINE</span></span>  <br/> |<span data-ttu-id="3709b-408">0 x 00000100</span><span class="sxs-lookup"><span data-stu-id="3709b-408">0x00000100</span></span>  <br/> |<span data-ttu-id="3709b-409">Wenn Outlook im Exchange-Cache-Modus ist, kann ein Client oder Dienstanbieter rufen die [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) -Methode, in den _UlFlags_ -Parameter, um die Verbindung zu den lokalen Nachrichtenspeicher überschreiben, und öffnen Sie das **MDB_ONLINE** -Flag festlegen der Speicher auf dem Remoteserver.</span><span class="sxs-lookup"><span data-stu-id="3709b-409">If Outlook is in Cached Exchange Mode, a client or service provider can call the [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) method, setting the **MDB_ONLINE** flag in the  _ulFlags_ parameter to override the connection to the local message store and open the store on the remote server.</span></span> <span data-ttu-id="3709b-410">Beachten Sie, dass Sie einen Exchange-Speicher im Cache-Modus und im nicht-Cache-Modus gleichzeitig in derselben MAPI-Sitzung nicht öffnen können.</span><span class="sxs-lookup"><span data-stu-id="3709b-410">Note that you cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="3709b-411">Wenn Sie den zwischengespeicherten Nachrichtenspeicher bereits geöffnet haben, müssen Sie entweder den Speicher schließen, bevor Sie dieses Flag zu öffnen, oder öffnen eine neue MAPI-Sitzung, in dem Sie den Exchange-Speicher auf dem Remoteserver mithilfe dieses Flag öffnen können.</span><span class="sxs-lookup"><span data-stu-id="3709b-411">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>  <br/> |
|<span data-ttu-id="3709b-412">NON_EMS_XP_SAVE</span><span class="sxs-lookup"><span data-stu-id="3709b-412">NON_EMS_XP_SAVE</span></span>  <br/> |<span data-ttu-id="3709b-413">0 x 00001000</span><span class="sxs-lookup"><span data-stu-id="3709b-413">0x00001000</span></span>  <br/> |<span data-ttu-id="3709b-414">Ein Client kann die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aufrufen und das Flag **NON_EMS_XP_SAVE** in der _UlFlags_ -Parameter, um anzugeben, dass die Nachricht von einem Exchange-Server nicht zugestellt wurde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3709b-414">A client can call the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method, setting the **NON_EMS_XP_SAVE** flag in the  _ulFlags_ parameter to indicate that the message has not been delivered from an Exchange server.</span></span> <span data-ttu-id="3709b-415">Dieses Kennzeichen sollte verwendet werden in Kombination mit dem im Parameter _UlFlags_ **ITEMPROC_FORCE** -Flag an, dass eine PST-Speicher, der die Nachricht für Regeln verarbeiten, bevor Sie die PST-Datei ist Speicher jeder listening Client über den Empfang von informiert die Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3709b-415">This flag should be used in combination with the **ITEMPROC_FORCE** flag in the  _ulFlags_ parameter to indicate to a PST store that the message is eligible for rules processing before the PST store notifies any listening client of the arrival of the message.</span></span> <span data-ttu-id="3709b-416">Die Regel, dass nur Verarbeitung auf neue Nachrichten angewendet wird, die mit [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) auf einem Server, die keinem Exchange-Server erstellt werden (in diesem Fall der Exchange-Server bereits Regeln für die Nachricht verarbeitet haben würde) ist.</span><span class="sxs-lookup"><span data-stu-id="3709b-416">This rules processing only applies to new messages that are created with [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) on a server that is not an Exchange server (in which case the Exchange server would have already processed rules on the message).</span></span>  <br/> |
|<span data-ttu-id="3709b-417">SPAMFILTER_ONSAVE</span><span class="sxs-lookup"><span data-stu-id="3709b-417">SPAMFILTER_ONSAVE</span></span>  <br/> |<span data-ttu-id="3709b-418">0x00000080</span><span class="sxs-lookup"><span data-stu-id="3709b-418">0x00000080</span></span>  <br/> |<span data-ttu-id="3709b-419">Ein Client kann Aufrufen [IMAPIProp::SaveChanges](imapiprop-savechanges.md), das **SPAMFILTER_ONSAVE** -Flag festlegen, in der _UlFlags_ -Parameter zum Aktivieren der Spamfilterung für eine Nachricht ein, die gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="3709b-419">A client can call [IMAPIProp::SaveChanges](imapiprop-savechanges.md), setting the **SPAMFILTER_ONSAVE** flag in the  _ulFlags_ parameter to enable spam filtering on a message that is being saved.</span></span> <span data-ttu-id="3709b-420">Unterstützung der Spamfilterung steht nur, wenn der Absender e-Mail-Adresstyp Simple Mail Transfer Protocol (SMTP ist), und die Nachricht einen Speicher für Persönliche Ordner-Datei (PST) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3709b-420">Spam filtering support is available only if the sender's email address type is Simple Mail Transfer Protocol (SMTP), and the message is being saved to a store for a Personal Folders file (PST).</span></span>  <br/> |
|<span data-ttu-id="3709b-421">STORE_ITEMPROC</span><span class="sxs-lookup"><span data-stu-id="3709b-421">STORE_ITEMPROC</span></span>  <br/> |<span data-ttu-id="3709b-422">0x00200000</span><span class="sxs-lookup"><span data-stu-id="3709b-422">0x00200000</span></span>  <br/> |<span data-ttu-id="3709b-423">Wenn in der [PidTagStoreSupportMask kanonische-Eigenschaft](pidtagstoresupportmask-canonical-property.md) eines gepackten PST-Speichers dieses Flag festgelegt ist, bedeutet dies, dass beim Empfang einer neuen Nachricht an den Speicher der Informationsspeicher verfügt über Regeln und Filtern von Spam separat auf die Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="3709b-423">If this flag is set in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md) of a wrapped PST store, it indicates that when a new message arrives at the store, the store has rules and spam filtering processed on the message separately.</span></span> <span data-ttu-id="3709b-424">Der Informationsspeicher ruft dann [IMAPISupport::Notify](imapisupport-notify.md), Festlegen von **FnevNewMail** in der [Benachrichtigung](notification.md) -Struktur, die als Parameter übergeben wird, und übergeben die Details der neuen Nachricht an einem Client listening.</span><span class="sxs-lookup"><span data-stu-id="3709b-424">The store then calls [IMAPISupport::Notify](imapisupport-notify.md), setting **fnevNewMail** in the [NOTIFICATION](notification.md) structure that is passed as a parameter, and passing the details of the new message to a listening client.</span></span> <span data-ttu-id="3709b-425">Später, wenn der listening Client die Benachrichtigung erhält, verarbeitet es Regeln für die Nachricht nicht.</span><span class="sxs-lookup"><span data-stu-id="3709b-425">Subsequently, when the listening client receives the notification, it does not process rules on the message.</span></span>  <br/> |
|<span data-ttu-id="3709b-426">STORE_UNICODE_OK</span><span class="sxs-lookup"><span data-stu-id="3709b-426">STORE_UNICODE_OK</span></span>  <br/> |<span data-ttu-id="3709b-427">0 x 00040000</span><span class="sxs-lookup"><span data-stu-id="3709b-427">0x00040000</span></span>  <br/> |<span data-ttu-id="3709b-428">Wenn dieses Flag in der [PidTagStoreSupportMask kanonische-Eigenschaft](pidtagstoresupportmask-canonical-property.md)enthalten ist, bedeutet dies, dass der Informationsspeicher Unicode-Speicher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3709b-428">If this flag is included in the [PidTagStoreSupportMask Canonical Property](pidtagstoresupportmask-canonical-property.md), it indicates that the store supports Unicode storage.</span></span> <span data-ttu-id="3709b-429">Ein Client kann für das Vorhandensein des Flags entscheiden, ob anfordern oder Unicode-Informationen im Speicher speichern aussehen.</span><span class="sxs-lookup"><span data-stu-id="3709b-429">A client can look for the presence of the flag to decide whether to request or to save Unicode information to the store.</span></span>  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a><span data-ttu-id="3709b-430">Definitionen für die Archivierung von Elementen in einem Ordner</span><span class="sxs-lookup"><span data-stu-id="3709b-430">Definitions for archiving items in a folder</span></span>

<span data-ttu-id="3709b-431">Die folgenden Konstantendefinitionen sind an die [Kanonische PidTagAgingGranularity-Eigenschaft](pidtagaginggranularity-canonical-property.md)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3709b-431">The following constant definitions are values used to set the [PidTagAgingGranularity Canonical Property](pidtagaginggranularity-canonical-property.md).</span></span>
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a><span data-ttu-id="3709b-432">Definitionen für die Anzeige von remote-Objekte</span><span class="sxs-lookup"><span data-stu-id="3709b-432">Definitions for displaying remote objects</span></span>

<span data-ttu-id="3709b-433">Die folgenden Konstanten und Makro Definitionen sind für die Anzeige von remote-Objekte.</span><span class="sxs-lookup"><span data-stu-id="3709b-433">The following constant and macro definitions are for displaying remote objects.</span></span> <span data-ttu-id="3709b-434">Weitere Informationen finden Sie unter der [PidTagDisplayTypeEx kanonische-Eigenschaft](pidtagdisplaytypeex-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="3709b-434">For more information, see the [PidTagDisplayTypeEx Canonical Property](pidtagdisplaytypeex-canonical-property.md).</span></span>
  
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

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a><span data-ttu-id="3709b-435">Definitionen für Exchange-Adressbuch und Nachricht speichern Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3709b-435">Definitions for Exchange address book and Message store error codes</span></span>

<span data-ttu-id="3709b-436">Die folgenden enthält Definitionen der Fehlercodes für die Exchange-Adressbuch und Nachrichtenspeicher, die wiederhergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="3709b-436">The following contains error code definitions for the Exchange Address Book and Message Store, which have reconnection capability.</span></span> <span data-ttu-id="3709b-437">Der letzte Aufruf an einen getrennten Global Catalog (GC) möglicherweise den Fehler **MAPI_E_END_OF_SESSION** die erneut ausgeführt werden müssen, würde.</span><span class="sxs-lookup"><span data-stu-id="3709b-437">The last call to a disconnected Global Catalog (GC) may result in the **MAPI_E_END_OF_SESSION** error, which would need to be retried.</span></span> 
  
<span data-ttu-id="3709b-438">Outlook MAPI unterstützt wiederhergestellt werden auf einem globalen Katalogserver ohne spezielle Neukonfiguration, aber ein anderer Fehler Codes an den Client zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="3709b-438">Outlook's MAPI supports reconnection to a GC server without special reconfiguration, but some other error codes can be returned to the client.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="3709b-439">MAPI_E_END_OF_SESSION</span><span class="sxs-lookup"><span data-stu-id="3709b-439">MAPI_E_END_OF_SESSION</span></span>  <br/> |<span data-ttu-id="3709b-440">0x80040200</span><span class="sxs-lookup"><span data-stu-id="3709b-440">0x80040200</span></span>  <br/> |<span data-ttu-id="3709b-441">Zurückgegeben, wenn eine Verbindung getrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="3709b-441">Returned when a connection has been disconnected.</span></span>  <br/> |
|<span data-ttu-id="3709b-442">MAPI_E_RECONNECTED</span><span class="sxs-lookup"><span data-stu-id="3709b-442">MAPI_E_RECONNECTED</span></span>  <br/> |<span data-ttu-id="3709b-443">0x80040125</span><span class="sxs-lookup"><span data-stu-id="3709b-443">0x80040125</span></span>  <br/> |<span data-ttu-id="3709b-444">Zurückgegeben, wenn das Connection-Token (Remote Procedure Call, RPC) veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="3709b-444">Returned when the Remote Procedure Call (RPC) connection token is out-of-date.</span></span> <span data-ttu-id="3709b-445">Wenn das Token für die aktuelle Transaktion anders ist der Verbindung, die sie bedeutet, dass das Token wurde wiederhergestellt, damit **MAPI_E_RECONNECTED** zurückgegeben und dürfen wie **MAPI_E_END_OF_SESSION**behandelt.</span><span class="sxs-lookup"><span data-stu-id="3709b-445">If the token of the current transaction is different from the token of the connection that means it has reconnected, so **MAPI_E_RECONNECTED** is returned and can be treated the same as **MAPI_E_END_OF_SESSION**.</span></span> <span data-ttu-id="3709b-446">Der Anruf sollte wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="3709b-446">The call should be retried.</span></span>  <br/> |
|<span data-ttu-id="3709b-447">MAPI_E_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="3709b-447">MAPI_E_OFFLINE</span></span>  <br/> |<span data-ttu-id="3709b-448">0x80040126</span><span class="sxs-lookup"><span data-stu-id="3709b-448">0x80040126</span></span>  <br/> |<span data-ttu-id="3709b-449">Zurückgegeben, wenn die Verbindung offline ist.</span><span class="sxs-lookup"><span data-stu-id="3709b-449">Returned when the connection is offline.</span></span> <span data-ttu-id="3709b-450">Dies bedeutet normalerweise, dass etwas in der Umgebung, wie Serverausfall oder Netzwerkkonnektivität aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="3709b-450">Typically this means that something has occurred in the environment, such as server failure or loss of network connectivity.</span></span> <span data-ttu-id="3709b-451">Dieser Fehler wird vor allem auftreten, wenn einen-Cache-Modus verwendet Profil und versucht, den Cache zur Kommunikation mit dem Server zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="3709b-451">This error is most likely to occur when using a cached mode profile and attempting to bypass the cache to communicate with the server.</span></span> <span data-ttu-id="3709b-452">Befand sich der Cache nie zunächst eine Verbindung mit dem Server herstellen können, kann es in den Offlinemodus sein, in dem **MAPI_E_OFFLINE** Offenlegen konnte.</span><span class="sxs-lookup"><span data-stu-id="3709b-452">If the cache was never able to initially establish a connection to the server, it may be in the offline state in which **MAPI_E_OFFLINE** could surface.</span></span>  <br/> |
   
<span data-ttu-id="3709b-453">Keines der vorhergehenden zwei Fehler wird in allen Szenarien zurückgegeben werden soll, auf dem würden sie wahrscheinlich angezeigt werden angewendet.</span><span class="sxs-lookup"><span data-stu-id="3709b-453">Neither of the preceding two errors will be returned in all scenarios where they would likely appear to apply.</span></span> <span data-ttu-id="3709b-454">In den meisten Fällen **MAPI\_E_NETWORK_ERROR** oder **MAPI_E_CALL_FAILED** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3709b-454">In most cases, **MAPI\_E_NETWORK_ERROR** or **MAPI_E_CALL_FAILED** will be returned.</span></span> <span data-ttu-id="3709b-455">Weder wird angezeigt, mit der [Microsoft Exchange Server-MAPI-Client und Collaboration Data Objects 1.2.1 (engl.)](http://support.microsoft.com/kb/171440) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="3709b-455">Neither will appear using the [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](http://support.microsoft.com/kb/171440) download.</span></span> 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a><span data-ttu-id="3709b-456">Definitionen für Exchange Server-Postfach-Cache-Modus von Kontingenten</span><span class="sxs-lookup"><span data-stu-id="3709b-456">Definitions for Exchange Server Mailbox cached mode quotas</span></span>

<span data-ttu-id="3709b-457">Die folgenden Konstantendefinitionen werden von Microsoft Outlook 2010 und Microsoft Outlook 2013, legen Sie den Exchange-Cache-Modus Profil Kontingente, die die Exchange-Postfachkontingente andernfalls nur mit einem online Profil verfügbaren entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3709b-457">The following constant definitions are used by Microsoft Outlook 2010 and Microsoft Outlook 2013 to set the Exchange cached mode profile quotas that are equivalent to the Exchange mailbox quotas otherwise available only with an online profile.</span></span>
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

<span data-ttu-id="3709b-458">Diese Eigenschaften zuordnen, deren Verlaufsattribut online Eigenschaften und enthalten dieselben Werte wie in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="3709b-458">These properties map to their correspondent online properties and contain the same values in kilobytes.</span></span> <span data-ttu-id="3709b-459">PR_QUOTA_WARNING ordnet PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND, PR_QUOTA_PROHIBIT_SEND_QUOTA und PR_QUOTA_RECEIVE auf PR_PROHIBIT_RECEIVE_QUOTA.</span><span class="sxs-lookup"><span data-stu-id="3709b-459">PR_QUOTA_WARNING maps to PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND to PR_QUOTA_PROHIBIT_SEND_QUOTA, and PR_QUOTA_RECEIVE to PR_PROHIBIT_RECEIVE_QUOTA.</span></span>
  
### <a name="definitions-for-message-format"></a><span data-ttu-id="3709b-460">Definitionen für Nachrichtenformat</span><span class="sxs-lookup"><span data-stu-id="3709b-460">Definitions for message format</span></span>

<span data-ttu-id="3709b-461">Die folgenden Konstantendefinitionen sind Werte, mit denen die [Kanonische PidTagMessageEditorFormat-Eigenschaft](pidtagmessageeditorformat-canonical-property.md)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3709b-461">The following constant definitions are values that are used to set the [PidTagMessageEditorFormat Canonical Property](pidtagmessageeditorformat-canonical-property.md).</span></span>
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a><span data-ttu-id="3709b-462">Definitionen für die Verwendung von RPC über HTTP</span><span class="sxs-lookup"><span data-stu-id="3709b-462">Definitions for using RPC over HTTP</span></span>

<span data-ttu-id="3709b-463">Finden Sie im Thema [PidTagRpcOverHttpFlags kanonische-Eigenschaft](pidtagrpcoverhttpflags-canonical-property.md) Konstantendefinitionen als Flags verwendet, um die-Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3709b-463">See the [PidTagRpcOverHttpFlags Canonical Property](pidtagrpcoverhttpflags-canonical-property.md) topic for constant definitions used as flags to set the property.</span></span> 
  
<span data-ttu-id="3709b-464">Finden Sie im Thema [PidTagRpcOverHttpProxyAuthScheme kanonische-Eigenschaft](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) Konstantendefinitionen verwendet, um die Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3709b-464">See the [PidTagRpcOverHttpProxyAuthScheme Canonical Property](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) topic for constant definitions used to set the property.</span></span> 
  
### <a name="identifiers"></a><span data-ttu-id="3709b-465">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="3709b-465">Identifiers</span></span>

<span data-ttu-id="3709b-466">Verwendung der `DEFINE_OLEGUID` Makro in der Microsoft Windows Software Development Kit (SDK) Header-Datei guiddef.h, ordnen Sie die folgenden GUID symbolischen Namen mit ihren Werten definiert.</span><span class="sxs-lookup"><span data-stu-id="3709b-466">Use the  `DEFINE_OLEGUID` macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate the following GUID symbolic names with their values.</span></span> 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

<span data-ttu-id="3709b-467">Der folgende Bezeichner ist für den Abschnitt Capone Profil ein Adressbuch, die zur Unterstützung mehrerer Postfächer von Exchange ([MultiEx](using-multiple-exchange-accounts.md)) eine [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) -Eigenschaft enthält, die die Standardeinstellung effektiv deaktiviert mit [SetDefaultDir](iaddrbook-setdefaultdir.md)angegebenen Container.</span><span class="sxs-lookup"><span data-stu-id="3709b-467">The following Identifier is for the Capone Profile section of an Address Book, which in support of multiple Exchange ([MultiEx](using-multiple-exchange-accounts.md)) mailboxes contains a [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) property that effectively turns off the default container specified by [SetDefaultDir](iaddrbook-setdefaultdir.md).</span></span>
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a><span data-ttu-id="3709b-468">Schnittstelle-IDs</span><span class="sxs-lookup"><span data-stu-id="3709b-468">Interface identifiers</span></span>

#### <a name="imapisync"></a><span data-ttu-id="3709b-469">IMAPISync</span><span class="sxs-lookup"><span data-stu-id="3709b-469">IMAPISync</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a><span data-ttu-id="3709b-470">IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="3709b-470">IMAPISyncProgressCallback</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iidicontabadmin"></a><span data-ttu-id="3709b-471">IID_IContabAdmin</span><span class="sxs-lookup"><span data-stu-id="3709b-471">IID_IContabAdmin</span></span>
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iidimapisecuremessage"></a><span data-ttu-id="3709b-472">IID_IMAPISECUREMESSAGE</span><span class="sxs-lookup"><span data-stu-id="3709b-472">IID_IMAPISECUREMESSAGE</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iidimapigetsession"></a><span data-ttu-id="3709b-473">IID_IMAPIGetSession</span><span class="sxs-lookup"><span data-stu-id="3709b-473">IID_IMAPIGetSession</span></span>
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a><span data-ttu-id="3709b-474">PST-Datei überschreiben Handler Schnittstelle-IDs</span><span class="sxs-lookup"><span data-stu-id="3709b-474">PST Override Handler interface identifiers</span></span>

#### <a name="iidipstoverridereq"></a><span data-ttu-id="3709b-475">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="3709b-475">IID_IPSTOVERRIDEREQ</span></span>
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iidipstoverride1"></a><span data-ttu-id="3709b-476">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="3709b-476">IID_IPSTOVERRIDE1</span></span>
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a><span data-ttu-id="3709b-477">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3709b-477">See also</span></span>

- [<span data-ttu-id="3709b-478">Informationen zu MAPI-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="3709b-478">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="3709b-479">Informationen zu benannten Eigenschaften in Outlook</span><span class="sxs-lookup"><span data-stu-id="3709b-479">About Named Properties Used by Outlook</span></span>](about-named-properties-used-by-outlook.md)
- [<span data-ttu-id="3709b-480">Zugreifen auf einen Store auf dem Remote-Server, wenn Outlook sich Exchange-Cache-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="3709b-480">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="3709b-481">Öffnen eines Speichers auf dem Remote-Server, wenn Outlook sich im Exchange-Cache-Modus befindet</span><span class="sxs-lookup"><span data-stu-id="3709b-481">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="3709b-482">Verwalten einer Nachricht in einem OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus</span><span class="sxs-lookup"><span data-stu-id="3709b-482">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

