---
title: MAPI-Konstanten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8fa5ac8d-3f63-499c-bb4e-439984773e4a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d6d6c55776c1379ec1dab0e9a6f7ef0943d2480e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792973"
---
# <a name="mapi-constants"></a>MAPI-Konstanten

**Betrifft**: Outlook 
  
Dieses Thema enthält Konstantendefinitionen, MAPI-Schnittstellendeklarationen und -Klasse und Schnittstelle Bezeichner, die von der MAPI-APIs verwendet.
  
## <a name="class-and-interface-identifiers"></a>Bezeichner-Klasse und Schnittstelle

Verwenden Sie das DEFINE_GUID-Makro in der Microsoft Windows Software Development Kit (SDK)-Header-Datei guiddef.h definiert, deren Werte symbolische Namen global eindeutigen Bezeichner (GUID) zugeordnet, sofern nichts anderes angegeben ist.
  
## <a name="attachment-security-conversion-api"></a>Anlage Sicherheit Konvertierung API

Dieser Abschnitt enthält Konstantendefinitionen und Schnittstellenbezeichner für die Anlage Security-API.
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

Verwenden Sie das MAPIMETHOD Makro in der Windows SDK-Header-Datei mapidefs.h definiert, um die reinen virtuellen Funktion **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)** definieren. 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

Verwenden Sie DECLARE_MAPI_INTERFACE_ Makros in der Windows SDK-Header-Datei mapidefs.h definiert, um die Tabelle virtueller Methoden für **["IAttachmentSecurity"](iattachmentsecurityiunknown.md)** definieren. 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a>MAPI-MIME-Konvertierung API

Dieser Abschnitt enthält Konstantendefinitionen und -Klasse und Schnittstelle Bezeichner für die MAPI-MIME-Konvertierung-API.
  
### <a name="constants"></a>Konstanten

|||
|:-----|:-----|
|CCSF_SMTP  <br/> |0x0002  <br/> |
|CCSF_NOHEADERS  <br/> |0x0004  <br/> |
|CCSF_USE_TNEF  <br/> | 0x0010  <br/> |
|CCSF_INCLUDE_BCC  <br/> |0 x 0020  <br/> |
|CCSF_8BITHEADERS  <br/> | 0x0040  <br/> |
|CCSF_USE_RTF  <br/> |0 x 0080  <br/> |
|CCSF_PLAIN_TEXT_ONLY  <br/> |0 x 1000  <br/> |
|CCSF_NO_MSGID  <br/> |0 x 4000  <br/> |
|E_INVALIDARG  <br/> | *Wie in der Microsoft Windows Software Development Kit (SDK) Headerdatei winerror.h definiert*  <br/> |
   
### <a name="class-identifiers"></a>Class Identifier

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a>Schnittstelle-IDs

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a>Offline-Status-API

Dieser Abschnitt enthält Konstantendefinitionen und -Klasse und Schnittstelle Bezeichner für Zustand-API.
  
### <a name="constants"></a>Konstanten

|||
|:-----|:-----|
|E_INVALIDARG  <br/> | *Wie in der Microsoft Windows Software Development Kit (SDK) Headerdatei winerror.h definiert*  <br/> |
|E_NOINTERFACE  <br/> | *Gemäß Definition in der Headerdatei winerror.h Windows (SDK)*  <br/> |
|MAPIOFFLINE_ADVISE_DEFAULT  <br/> |(ULONG) 0  <br/> |
|MAPIOFFLINE_UNADVISE_DEFAULT  <br/> |(ULONG) 0  <br/> |
|MAPIOFFLINE_ADVISE_TYPE_STATECHANGE  <br/> |1  <br/> |
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |0 x 1  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |0 x 2  <br/> |
|MAPIOFFLINE_FLAG_BLOCK  <br/> |0 x 00002000  <br/> |
|MAPIOFFLINE_FLAG_DEFAULT  <br/> |0x00000000  <br/> |
|MAPIOFFLINE_STATE_ALL  <br/> |0x003f037f  <br/> |
|**Online oder offline** <br/> ||
|MAPIOFFLINE_STATE_OFFLINE_MASK  <br/> |0 x 00000003  <br/> |
|MAPIOFFLINE_STATE_OFFLINE  <br/> |0x00000001  <br/> |
|MAPIOFFLINE_STATE_ONLINE  <br/> |0x00000002  <br/> |
   
### <a name="class-identifiers"></a>Class Identifier

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a>Schnittstelle-IDs

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

## <a name="outlook-named-properties"></a>Benannte Eigenschaften Outlook

Dieser Abschnitt enthält Konstantendefinitionen für benannte Eigenschaften und deren Namespaces und andere zugehörigen-Konstanten.
  
### <a name="definitions-for-named-properties"></a>Definitionen für benannte Eigenschaften

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

### <a name="definitions-for-namespaces"></a>Definitionen für namespaces

Die folgenden global eindeutigen Bezeichner (GUIDs) repräsentieren die Namespaces der benannten Eigenschaften.
  
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

Finden Sie im Abschnitt MAPI-Speicher für die PSETID-Definitionen.
  
### <a name="other-constants"></a>Anderen-Konstanten

|||
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0xD000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x2000000  <br/> |
|MNID_ID  <br/> | *Wie in der Header-Datei mapidefs.h definiert.*  <br/> |
|MNID_STRING  <br/> | *Wie in der Header-Datei mapidefs.h definiert.*  <br/> |
|mtgNone  <br/> |0 x 0  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |
|mtgFullUpdate  <br/> |0 x 00010000  <br/> |
|mtgInfoUpdate  <br/> |0 x 00020000  <br/> |
|mtgOutofDate  <br/> |0x00080000  <br/> |
|mtgDelegated  <br/> |0x00100000  <br/> |
   
## <a name="replication-api"></a>Replikations-API

Dieser Abschnitt enthält Konstantendefinitionen, MAPI-Schnittstellendeklarationen und -Klasse und Schnittstelle Bezeichner für die Replikation-API.
  
### <a name="constants"></a>Konstanten

Es folgt eine [MAPIUID](mapiuid.md) -Struktur, die einen MAPI-Dienstanbieter identifiziert: 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|DNH_OK  <br/> |0 x 00010000  <br/> |
|DNT_OK  <br/> |0 x 00010000  <br/> |
|HSF_LOCAL  <br/> |0 x 00000008  <br/> |
|HSF_COPYDESTRUCTIVE  <br/> |0 x 00000010  <br/> |
|HSF_OK  <br/> |0 x 00010000  <br/> |
|MDB_OST_LOGON_UNICODE  <br/> |((ULONG) 0X00000800)  <br/> |
|MDB_OST_LOGON_ANSI  <br/> |((ULONG) 0 X 00001000)  <br/> |
|SHOW_SOFT_DELETES  <br/> |((ULONG) 0 X 00000002)  <br/> |
|SS_ACTIVE  <br/> |0  <br/> |
|SS_SUSPENDED  <br/> |1  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0 x 00000040  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |
|SYNC_OUTGOING_MAIL  <br/> |0 x 00000200  <br/> |
|SYNC_BACKGROUND  <br/> |0 x 00001000  <br/> |
|SYNC_THESE_FOLDERS  <br/> |0 x 00020000  <br/> |
|SYNC_HEADERS  <br/> |0x02000000  <br/> |
|UPC_OK  <br/> |0 x 00010000  <br/> |
|UPD_ASSOC  <br/> |0x00000001  <br/> |
|UPD_MOV  <br/> |0x00000002  <br/> |
|UPD_OK  <br/> |0 x 00010000  <br/> |
|UPD_MOVED  <br/> |0 x 00020000  <br/> |
|UPD_UPDATE  <br/> |0 x 00040000  <br/> |
|UPD_COMMIT  <br/> |0x00080000  <br/> |
|UPF_NEW  <br/> |0x00000001  <br/> |
|UPF_MOD_PARENT  <br/> |0x00000002  <br/> |
|UPF_MOD_PROPS  <br/> |0 x 00000004  <br/> |
|UPF_DEL  <br/> |0 x 00000008  <br/> |
|UPF_OK  <br/> |0 x 00010000  <br/> |
|UPH_OK  <br/> |0 x 00010000  <br/> |
|UPM_ASSOC  <br/> |0x00000001  <br/> |
|UPM_NEW  <br/> |0x00000002  <br/> |
|UPM_MOV  <br/> |0 x 00000004  <br/> |
|UPM_MOD_PROPS  <br/> |0 x 00000008  <br/> |
|UPM_HEADER  <br/> |0 x 00000010  <br/> |
|UPM_OK  <br/> |0 x 00010000  <br/> |
|UPM_MOVED  <br/> |0 x 00020000  <br/> |
|UPM_COMMIT  <br/> |0 x 00040000  <br/> |
|UPM_DELETE  <br/> |0x00080000  <br/> |
|UPM_SAVE  <br/> |0x00100000  <br/> |
|UPR_ASSOC  <br/> |0x00000001  <br/> |
|UPR_READ  <br/> |0x00000002  <br/> |
|UPR_OK  <br/> |0 x 00010000  <br/> |
|UPR_COMMIT  <br/> |0 x 00020000  <br/> |
|UPS_UPLOAD_ONLY  <br/> |0x00000001  <br/> |
|UPS_DNLOAD_ONLY  <br/> |0x00000002  <br/> |
|UPS_ONE_FOLDER  <br/> |0 x 00000004  <br/> |
|UPS_THESE_FOLDERS  <br/> |0x00000080  <br/> |
|UPS_OK  <br/> |0 x 00010000  <br/> |
|UPT_OK  <br/> |0 x 00010000  <br/> |
|UPT_PUBLIC  <br/> |0x00000001  <br/> |
|UPV_ERROR  <br/> |0 x 00010000  <br/> |
|UPV_DIRTY  <br/> |0 x 00020000  <br/> |
|UPV_COMMIT  <br/> |0 x 00040000  <br/> |
   
### <a name="interface-declarations"></a>Schnittstellendeklarationen

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a>Schnittstelle-IDs

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

Verwenden Sie die folgende Schnittstellenbezeichner mit [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md)oder [IMsgStore::OpenEntry](imsgstore-openentry.md) öffnen und alle Kontrollkästchen Anbieter auf ein Folder-Objekt und ein Meldungsobjekt jeweils ignorieren. 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a>MAPI-Speicher

Dieser Abschnitt enthält Konstantendefinitionen und Schnittstellenbezeichner vom verwendet APIs Schnittstelle mit einem MAPI-Speicher.
  
### <a name="constants"></a>Konstanten

||||
|:-----|:-----|:-----|
|fnevIndexing  <br/> |((ULONG) 0 X 00010000)  <br/> |Ein Anbieter anmelden kann **FnevIndexing** Geben Sie im **UlEventType** Member der Struktur **[Benachrichtigung](notification.md)** um der Indizierung zu benachrichtigen, dass ein Objekt für die Indizierung bereit ist. Der **Info** -Member der Struktur **Benachrichtigung** enthält eine **[EXTENDED_NOTIFICATION](extended_notification.md)** -Struktur.  <br/> |
|FS_NONE  <br/> |0 x 00  <br/> |Ein Client kann **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** und die Kontrollkästchen für die zurückgegebene Bitmaske aufrufen. **FS_NONE** gibt an, dass der Ordner Freigabe nicht unterstützt.  <br/> |
|FS_SUPPORTS_SHARING  <br/> |0x01  <br/> |Ein Client kann **IFolderSupport::GetSupportMask** und die Kontrollkästchen für die zurückgegebene Bitmaske aufrufen. **FS_SUPPORTS_SHARING** gibt an, dass der Ordner Freigabe unterstützt.  <br/> |
|INDEXING_SEARCH_OWNER  <br/> |((ULONG) 0 X 00000001)  <br/> |Identifiziert den Prozess, der eine Benachrichtigung zu einem Indexer beschäftigt ist, dass ein Objekt für die Indizierung bereit ist.  <br/> |
|MNID_ID  <br/> |Wie in der Microsoft Windows Software Development Kit (SDK)-Header-Datei mapidefs.h definiert  <br/> |Ein Wert für das Feld **UlKind** der **[MAPINAMEID](mapinameid.md)** Struktur.  <br/> |
|MNID_STRING  <br/> |Wie in der Microsoft Windows Software Development Kit (SDK)-Header-Datei mapidefs.h definiert.  <br/> |Ein Wert für das Feld **UlKind** der **[MAPINAMEID](mapinameid.md)** Struktur.  <br/> |
|MSCAP_RES_ANNOTATION  <br/> |((ULONG) 0 X 00000001)  <br/> |Wenn ein Client für **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)** **MSCAP_SEL_RESTRICTION** *MscapSelector* angibt, können **GetCapabilities** dieser Wert zurück, wenn der Informationsspeicher ungültige Parameter in einer Einschränkung ignoriert.  <br/> |
|MSCAP_SECURE_FOLDER_HOMEPAGES  <br/> |((ULONG) 0 X 00000020)  <br/> |Wenn ein Client für **IMSCapabilities::GetCapabilities** **MSCAP_SEL_FOLDER** *MscapSelector* angibt, können **GetCapabilities** dieser Wert zurück, wenn der Informationsspeicher einen nicht standardmäßigen Speicher ist, der unterstützt von Ordnerhomepages.  <br/> |
|STORE_PUSHER_OK  <br/> |((ULONG) 0 X 00800000)  <br/> |Ein Client kann die Eigenschaft **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** bestimmen das Merkmal eines Nachrichtenspeichers abrufen. Wenn der Anbieter das Flag **STORE_PUSHER_OK** in der Bitmaske festlegt, bedeutet, dass der MAPI-Protokollhandler wird nicht durchforstet werden den Speicher und der Speicher wird zum Pushen von Änderungen durch Benachrichtigungen auf die Indizierung Nachrichten indiziert werden.  <br/> |
   
### <a name="definitions-for-namespaces"></a>Definitionen für namespaces

Die folgenden global eindeutigen Bezeichner (GUIDs) repräsentieren die Namespaces der benannten Eigenschaften. Sie sind indiziert, durch die MAPI Protocol Handler (PH) und im schreibgeschützten Modus dokumentiert sind.
  
> [!CAUTION]
> Benannten Eigenschaften sollte nicht zum Erstellen oder Ändern von Elementen verwendet werden. 
  
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

#### <a name="mnidid-properties"></a>MNID_ID-Eigenschaften
  
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

#### <a name="mnidstring-properties"></a>MNID_STRING-Eigenschaften
  
```cpp
// In PS_PUBLIC_STRINGS 
"Keywords"
```

```cpp
// In PS_INTERNET_HEADERS
"return-path"
```

### <a name="interface-identifiers"></a>Schnittstelle-IDs

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

Verwendung der `DEFINE_OLEGUID` Makro definiert, in der Windows SDK-Header-Datei guiddef.h, dessen Wert den folgenden GUID symbolischen Name zugeordnet. 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a>MAPI-Adressbuch-Konstanten

Dieser Abschnitt enthält Konstantendefinitionen für das MAPI-Adressbuch.
  
### <a name="constants"></a>Konstanten

||||
|:-----|:-----|:-----|
|CONTAB_ROOT  <br/> |((ULONG) 0 X 00000001)  <br/> |Der Stammordner für ein MAPI-Address Book-Objekt.  <br/> |
|CONTAB_SUBROOT  <br/> |((ULONG) 0 X 00000002)  <br/> |Ein Unterordner in den Stammordner des MAPI-Address Book-Objekts enthalten sind.  <br/> |
|CONTAB_CONTAINER  <br/> |((ULONG) 0 X 00000003)  <br/> |Ein Address Book Container-Objekt.  <br/> |
|CONTAB_USER  <br/> |((ULONG) 0 X 00000004)  <br/> |Ein messaging User-Objekt.  <br/> |
|CONTAB_DISTLIST  <br/> |((ULONG) 0 X 00000005)  <br/> |Verteilung von List-Objekt.  <br/> |
   
## <a name="additional-mapi-constants"></a>Zusätzliche MAPI-Konstanten

Dieser Abschnitt enthält Konstantendefinitionen einschließlich Fehlercodes und Schnittstelle-IDs von MAPI-APIs, die zuvor nicht verfügbar gemacht und dokumentiert wurden verwendet.
  
||||
|:-----|:-----|:-----|
|DIALOG_MODAL  <br/> |((ULONG) 0 X 00000001)  <br/> |Wenn ein Client die [IAddrBook::Details](iaddrbook-details.md) -Methode aufruft, muss der Client das Flag **DIALOG_MODAL** im _UlFlags_ -Parameter zum Anzeigen des modalen Dialogfelds, das die Details zu einer bestimmten Adressbuch Adresseintrag festgelegt. Diese Konstante wird in mapidefs.h definiert.  <br/> |
|ITEMPROC_FORCE  <br/> |0x00000800  <br/> |In Outlook 2007 gepackten PST-Speicher verfügen, Regeln und Spamfilterung für neue Nachrichten verarbeitet, bevor der neuen Nachrichten MAPI-Clients benachrichtigt werden. Einen Anbieter oder -Client wird mithilfe der [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) -Methode zum Erstellen einer neuen Nachricht in PST-Speicher sollte das Flag **ITEMPROC_FORCE** im _UlFlags_ -Parameter der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode, um die PST-Datei anzugeben festgelegt. -Speichers, den die Nachricht ist für Regeln für die Verarbeitung, bevor der Speicher jeder listening Client die Ankunft der neuen Nachricht informiert. Beachten Sie, dass nur solche regelverarbeitung gilt für neue Nachrichten, die auf einem Server, der nicht auf einem Microsoft Exchange Server ist erstellt werden, da Exchange Server Regeln für Nachrichten auf dem Server verarbeitet. Daher muss vom Anbieter oder vom Client erstellen die Meldung dieses Flag in Kombination mit **NON_EMS_XP_SAVE**, übergeben Sie gibt an, dass der Server nicht mit einem Exchange-Server ist.  <br/> |
| MAPI_BG_SESSION  <br/> |0x00200000  <br/> |Ein Client kann die Funktion [MAPILogonEx](mapilogonex.md) aufrufen und Festlegen des Flags **MAPI_BG_SESSION** in den _FlFlags_ -Parameter, um eine Sitzung anmelden und Vorgänge im Hintergrund auszuführen. Ein Client will Verarbeitung in einem Hintergrundthread oder in einem gesonderten Prozess in einer Weise, die nicht störend auf den Vordergrundthread ist, sollte es im allgemeinen [MAPILogonEx](mapilogonex.md) mit dem **MAPI_BG_SESSION** -Flag aufrufen. Ein Beispiel, in dem Hiermit wird, ist eine Clientanwendung, wie etwa eine indexing-Engine, öffnen eine Persönliche Ordner Datei (PST) für den Hintergrund Typ Zugriff.  <br/> |
|MAPI_CACHE_ONLY  <br/> |0x00004000  <br/> |Ein Client kann die Methode [IAddrBook::OpenEntry](iaddrbook-openentry.md) aufrufen im Parameter _UlFlags_ ein Adresseintrags Adressbuch öffnen, und es anschließend nur aus dem Cache Zugriff auf das **MAPI_CACHE_ONLY** -Flag festlegen. Ein Beispiel, in dem dies verwendet wird, ist eine Clientanwendung, die zum Öffnen der globalen Adressliste im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server erstellen möchte.  <br/> |
|MAPI_DIALOG_MODELESS  <br/> |0x0000000C  <br/> |Dieser Wert kann der Simple MAPI MAPISendMail-Funktion in der _UlFlags_ -Parameter, um anzugeben, dass ein nicht modales Dialogfeld, von der standardmäßige e-Mail-Anwendung angezeigt wird übergeben werden. Wenn weder die MAPI_DIALOG (0 x 00000008) dieses Flag festgelegt ist, wird kein Dialogfeld angezeigt.  <br/> |
|MAPI_NO_CACHE  <br/> |0 x 00000200  <br/> |Wenn Microsoft Office Outlook im Exchange-Cache-Modus und ein Speicher im Cache-Modus geöffnet wurde, kann einen Client oder Dienstanbieter [IMsgStore::OpenEntry](imsgstore-openentry.md), das Flag **MAPI_NO_CACHE** in der _UlFlags_ -Parameter zum Öffnen eines Elements festgelegt anrufen oder eine Ordner auf den remote-Speicher. Beachten Sie, wenn Sie den Nachrichtenspeicher mit dem **MDB_ONLINE** -Flag auf dem Remoteserver öffnen, haben Sie nicht das Flag **MAPI_NO_CACHE** verwenden.  <br/> |
|PARAMETER MAPI_UNICODE  <br/> |0 x 80000000  <br/> |Ein Client oder Dienstanbieter kann die Funktion [OpenIMsgOnIStg](openimsgonistg.md) anrufen **die Option MAPI_UNICODE** im _UlFlags_ -Parameter zum Erstellen von Unicode MSG-Dateien festlegen. Das resultierende [IMessage: IMAPIProp](imessageimapiprop.md) Datei zeigt **STORE_UNICODE_OK** in seiner [PidTagStoreSupportMask kanonische-Eigenschaft](pidtagstoresupportmask-canonical-property.md) und unterstützt Unicode-Eigenschaften. Diese Konstante wird in mapidefs.h definiert.  <br/> |
|MDB_ONLINE  <br/> |0 x 00000100  <br/> |Wenn Outlook im Exchange-Cache-Modus ist, kann ein Client oder Dienstanbieter rufen die [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) -Methode, in den _UlFlags_ -Parameter, um die Verbindung zu den lokalen Nachrichtenspeicher überschreiben, und öffnen Sie das **MDB_ONLINE** -Flag festlegen der Speicher auf dem Remoteserver. Beachten Sie, dass Sie einen Exchange-Speicher im Cache-Modus und im nicht-Cache-Modus gleichzeitig in derselben MAPI-Sitzung nicht öffnen können. Wenn Sie den zwischengespeicherten Nachrichtenspeicher bereits geöffnet haben, müssen Sie entweder den Speicher schließen, bevor Sie dieses Flag zu öffnen, oder öffnen eine neue MAPI-Sitzung, in dem Sie den Exchange-Speicher auf dem Remoteserver mithilfe dieses Flag öffnen können.  <br/> |
|NON_EMS_XP_SAVE  <br/> |0 x 00001000  <br/> |Ein Client kann die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode aufrufen und das Flag **NON_EMS_XP_SAVE** in der _UlFlags_ -Parameter, um anzugeben, dass die Nachricht von einem Exchange-Server nicht zugestellt wurde festgelegt. Dieses Kennzeichen sollte verwendet werden in Kombination mit dem im Parameter _UlFlags_ **ITEMPROC_FORCE** -Flag an, dass eine PST-Speicher, der die Nachricht für Regeln verarbeiten, bevor Sie die PST-Datei ist Speicher jeder listening Client über den Empfang von informiert die Nachricht. Die Regel, dass nur Verarbeitung auf neue Nachrichten angewendet wird, die mit [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) auf einem Server, die keinem Exchange-Server erstellt werden (in diesem Fall der Exchange-Server bereits Regeln für die Nachricht verarbeitet haben würde) ist.  <br/> |
|SPAMFILTER_ONSAVE  <br/> |0x00000080  <br/> |Ein Client kann Aufrufen [IMAPIProp::SaveChanges](imapiprop-savechanges.md), das **SPAMFILTER_ONSAVE** -Flag festlegen, in der _UlFlags_ -Parameter zum Aktivieren der Spamfilterung für eine Nachricht ein, die gespeichert wird. Unterstützung der Spamfilterung steht nur, wenn der Absender e-Mail-Adresstyp Simple Mail Transfer Protocol (SMTP ist), und die Nachricht einen Speicher für Persönliche Ordner-Datei (PST) gespeichert werden.  <br/> |
|STORE_ITEMPROC  <br/> |0x00200000  <br/> |Wenn in der [PidTagStoreSupportMask kanonische-Eigenschaft](pidtagstoresupportmask-canonical-property.md) eines gepackten PST-Speichers dieses Flag festgelegt ist, bedeutet dies, dass beim Empfang einer neuen Nachricht an den Speicher der Informationsspeicher verfügt über Regeln und Filtern von Spam separat auf die Nachricht verarbeitet. Der Informationsspeicher ruft dann [IMAPISupport::Notify](imapisupport-notify.md), Festlegen von **FnevNewMail** in der [Benachrichtigung](notification.md) -Struktur, die als Parameter übergeben wird, und übergeben die Details der neuen Nachricht an einem Client listening. Später, wenn der listening Client die Benachrichtigung erhält, verarbeitet es Regeln für die Nachricht nicht.  <br/> |
|STORE_UNICODE_OK  <br/> |0 x 00040000  <br/> |Wenn dieses Flag in der [PidTagStoreSupportMask kanonische-Eigenschaft](pidtagstoresupportmask-canonical-property.md)enthalten ist, bedeutet dies, dass der Informationsspeicher Unicode-Speicher unterstützt. Ein Client kann für das Vorhandensein des Flags entscheiden, ob anfordern oder Unicode-Informationen im Speicher speichern aussehen.  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a>Definitionen für die Archivierung von Elementen in einem Ordner

Die folgenden Konstantendefinitionen sind an die [Kanonische PidTagAgingGranularity-Eigenschaft](pidtagaginggranularity-canonical-property.md)festgelegt.
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a>Definitionen für die Anzeige von remote-Objekte

Die folgenden Konstanten und Makro Definitionen sind für die Anzeige von remote-Objekte. Weitere Informationen finden Sie unter der [PidTagDisplayTypeEx kanonische-Eigenschaft](pidtagdisplaytypeex-canonical-property.md).
  
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

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a>Definitionen für Exchange-Adressbuch und Nachricht speichern Fehlercodes

Die folgenden enthält Definitionen der Fehlercodes für die Exchange-Adressbuch und Nachrichtenspeicher, die wiederhergestellt werden können. Der letzte Aufruf an einen getrennten Global Catalog (GC) möglicherweise den Fehler **MAPI_E_END_OF_SESSION** die erneut ausgeführt werden müssen, würde. 
  
Outlook MAPI unterstützt wiederhergestellt werden auf einem globalen Katalogserver ohne spezielle Neukonfiguration, aber ein anderer Fehler Codes an den Client zurückgegeben werden können.
  
||||
|:-----|:-----|:-----|
|MAPI_E_END_OF_SESSION  <br/> |0x80040200  <br/> |Zurückgegeben, wenn eine Verbindung getrennt wurde.  <br/> |
|MAPI_E_RECONNECTED  <br/> |0x80040125  <br/> |Zurückgegeben, wenn das Connection-Token (Remote Procedure Call, RPC) veraltet ist. Wenn das Token für die aktuelle Transaktion anders ist der Verbindung, die sie bedeutet, dass das Token wurde wiederhergestellt, damit **MAPI_E_RECONNECTED** zurückgegeben und dürfen wie **MAPI_E_END_OF_SESSION**behandelt. Der Anruf sollte wiederholt werden.  <br/> |
|MAPI_E_OFFLINE  <br/> |0x80040126  <br/> |Zurückgegeben, wenn die Verbindung offline ist. Dies bedeutet normalerweise, dass etwas in der Umgebung, wie Serverausfall oder Netzwerkkonnektivität aufgetreten ist. Dieser Fehler wird vor allem auftreten, wenn einen-Cache-Modus verwendet Profil und versucht, den Cache zur Kommunikation mit dem Server zu umgehen. Befand sich der Cache nie zunächst eine Verbindung mit dem Server herstellen können, kann es in den Offlinemodus sein, in dem **MAPI_E_OFFLINE** Offenlegen konnte.  <br/> |
   
Keines der vorhergehenden zwei Fehler wird in allen Szenarien zurückgegeben werden soll, auf dem würden sie wahrscheinlich angezeigt werden angewendet. In den meisten Fällen **MAPI\_E_NETWORK_ERROR** oder **MAPI_E_CALL_FAILED** zurückgegeben wird. Weder wird angezeigt, mit der [Microsoft Exchange Server-MAPI-Client und Collaboration Data Objects 1.2.1 (engl.)](http://support.microsoft.com/kb/171440) herunterladen. 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a>Definitionen für Exchange Server-Postfach-Cache-Modus von Kontingenten

Die folgenden Konstantendefinitionen werden von Microsoft Outlook 2010 und Microsoft Outlook 2013, legen Sie den Exchange-Cache-Modus Profil Kontingente, die die Exchange-Postfachkontingente andernfalls nur mit einem online Profil verfügbaren entsprechen.
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

Diese Eigenschaften zuordnen, deren Verlaufsattribut online Eigenschaften und enthalten dieselben Werte wie in Kilobyte. PR_QUOTA_WARNING ordnet PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND, PR_QUOTA_PROHIBIT_SEND_QUOTA und PR_QUOTA_RECEIVE auf PR_PROHIBIT_RECEIVE_QUOTA.
  
### <a name="definitions-for-message-format"></a>Definitionen für Nachrichtenformat

Die folgenden Konstantendefinitionen sind Werte, mit denen die [Kanonische PidTagMessageEditorFormat-Eigenschaft](pidtagmessageeditorformat-canonical-property.md)festgelegt.
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a>Definitionen für die Verwendung von RPC über HTTP

Finden Sie im Thema [PidTagRpcOverHttpFlags kanonische-Eigenschaft](pidtagrpcoverhttpflags-canonical-property.md) Konstantendefinitionen als Flags verwendet, um die-Eigenschaft festgelegt. 
  
Finden Sie im Thema [PidTagRpcOverHttpProxyAuthScheme kanonische-Eigenschaft](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) Konstantendefinitionen verwendet, um die Eigenschaft festzulegen. 
  
### <a name="identifiers"></a>Bezeichner

Verwendung der `DEFINE_OLEGUID` Makro in der Microsoft Windows Software Development Kit (SDK) Header-Datei guiddef.h, ordnen Sie die folgenden GUID symbolischen Namen mit ihren Werten definiert. 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

Der folgende Bezeichner ist für den Abschnitt Capone Profil ein Adressbuch, die zur Unterstützung mehrerer Postfächer von Exchange ([MultiEx](using-multiple-exchange-accounts.md)) eine [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) -Eigenschaft enthält, die die Standardeinstellung effektiv deaktiviert mit [SetDefaultDir](iaddrbook-setdefaultdir.md)angegebenen Container.
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a>Schnittstelle-IDs

#### <a name="imapisync"></a>IMAPISync
  
```cpp
DEFINE_GUID(IID_IMAPISync, 0x5024a385, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);

```

#### <a name="imapisyncprogresscallback"></a>IMAPISyncProgressCallback
  
```cpp
DEFINE_GUID(IID_IMAPISyncProgressCallback, 0x5024a386, 0x2d44, 0x486a,  0x81, 0xa8, 0x8f, 0xe, 0xcb, 0x60, 0x71, 0xdd);
```

#### <a name="iidicontabadmin"></a>IID_IContabAdmin
  
```cpp
// {CC6A3BA9-E7F5-4769-887B-34E190817BFC}
DEFINE_GUID(IID_IContabAdmin, 0xcc6a3ba9, 0xe7f5, 0x4769, 0x88, 0x7b, 0x34, 0xe1, 0x90, 0x81, 0x7b, 0xfc);

```

#### <a name="iidimapisecuremessage"></a>IID_IMAPISECUREMESSAGE
  
```cpp
DEFINE_GUID(IID_IMAPISecureMessage, 0x253cc320, 0xeab6, 0x11d0, 0x82, 0x22, 0, 0x60, 0x97, 0x93, 0x87, 0xea);

```

#### <a name="iidimapigetsession"></a>IID_IMAPIGetSession
  
```cpp
DEFINE_GUID(IID_IMAPIGetSession, 0x614ab435, 0x491d, 0x4f5b, 0xa8, 0xb4, 0x60, 0xeb, 0x3, 0x10, 0x30, 0xc6);

```

### <a name="pst-override-handler-interface-identifiers"></a>PST-Datei überschreiben Handler Schnittstelle-IDs

#### <a name="iidipstoverridereq"></a>IID_IPSTOVERRIDEREQ
  
```cpp
// {892EBC6D-24DC-4d90-BA48-C6CBEC14A86A}
DEFINE_GUID(IID_IPSTOVERRIDEREQ, 0x892ebc6d, 0x24dc, 0x4d90, 0xba, 0x48, 0xc6, 0xcb, 0xec, 0x14, 0xa8, 0x6a);
```

#### <a name="iidipstoverride1"></a>IID_IPSTOVERRIDE1
  
```cpp
// {FBB68D34-F561-44fb-A8CA-AE36696342CA}
DEFINE_GUID(IID_IPSTOVERRIDE1, 0xfbb68d34, 0xf561, 0x44fb, 0xa8, 0xca, 0xae, 0x36, 0x69, 0x63, 0x42, 0xca);
```

## <a name="see-also"></a>Siehe auch

- [Informationen zu MAPI-Ergänzungen](about-mapi-additions.md) 
- [Informationen zu benannten Eigenschaften in Outlook](about-named-properties-used-by-outlook.md)
- [Zugreifen auf einen Store auf dem Remote-Server, wenn Outlook sich Exchange-Cache-Modus befindet](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Öffnen eines Speichers auf dem Remote-Server, wenn Outlook sich im Exchange-Cache-Modus befindet](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Verwalten einer Nachricht in einem OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

