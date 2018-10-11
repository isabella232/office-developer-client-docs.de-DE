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
ms.openlocfilehash: dfc7d16cdb2f57d3f095ceea5fa1ba2eba2e3afe
ms.sourcegitcommit: b91294da1627f6580f52fd3867e2fec8073c6531
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/03/2018
ms.locfileid: "25362043"
---
# <a name="mapi-constants"></a>MAPI-Konstanten

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dieser Abschnitt enthält die Konstantendefinitionen, MAPI-Schnittstellendeklarationen und Klassen- und Schnittstellenbezeichner, die von den MAPI-APIs verwendet werden.
  
## <a name="class-and-interface-identifiers"></a>Klassen- und Schnittstellenbezeichner

Verwenden Sie das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef.h definierte DEFINE_GUID-Makro, um symbolischen GUID-Namen (Globally Unique Identifier) Ihre Werte zuzuordnen (falls nicht anders angegeben).
  
## <a name="attachment-security-conversion-api"></a>Anlagensicherheit-Konvertierungs-API

Dieser Abschnitt enthält Konstantendefinitionen und Schnittstellenbezeichner für die Anlagensicherheit-API.
  
```cpp
// {b2533636-c3f3-416f-bf04-aefe41abaae2}
DEFINE_GUID(IID_IAttachmentSecurity, 0xb2533636, 0xc3f3, 0x416f, 0xbf, 0x04, 0xae, 0xfe, 0x41, 0xab, 0xaa, 0xe2);
```

Verwenden Sie das in der Windows SDK-Headerdatei mapidefs.h definierte MAPIMETHOD-Makro, um die rein virtuelle Funktion **[IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md)** zu definieren. 
  
```cpp
#define MAPI_IATTACHMENTSECURITY_METHODS(IPURE)         MAPIMETHOD(IsAttachmentBlocked)         (LPCWSTR pwszFileName, BOOL *pfBlocked) IPURE;
```

Verwenden Sie das in der Windows SDK-Headerdatei mapidefs.h definierte DECLARE_MAPI_INTERFACE_-Makro, um die Tabelle virtueller Methoden für **[IAttachmentSecurity](iattachmentsecurityiunknown.md)** zu definieren. 
  
```cpp
DECLARE_MAPI_INTERFACE_(IAttachmentSecurity, IUnknown) 
{ 
    BEGIN_INTERFACE 
    MAPI_IUNKNOWN_METHODS(PURE) 
    MAPI_IATTACHMENTSECURITY_METHODS(PURE) 
};
```

## <a name="mapi-mime-conversion-api"></a>MAPI-MIME-Konvertierungs-API

Dieser Abschnitt enthält Konstantendefinitionen und Klassen- und Schnittstellenbezeichner für die MAPI-MIME-Konversations-API.
  
### <a name="constants"></a>Konstanten

|||
|:-----|:-----|
|CCSF_SMTP  <br/> |0x0002  <br/> |
|CCSF_NOHEADERS  <br/> |0x0004  <br/> |
|CCSF_USE_TNEF  <br/> | 0x0010  <br/> |
|CCSF_INCLUDE_BCC  <br/> |0x0020  <br/> |
|CCSF_8BITHEADERS  <br/> | 0x0040  <br/> |
|CCSF_USE_RTF  <br/> |0x0080  <br/> |
|CCSF_PLAIN_TEXT_ONLY  <br/> |0x1000  <br/> |
|CCSF_NO_MSGID  <br/> |0x4000  <br/> |
|CCSF_GLOBAL_MESSAGE  <br/> |0x00200000  <br/> |
|E_INVALIDARG  <br/> | *Wie in der Microsoft Windows Software Development Kit (SDK)-Headerdatei winerror.h definiert*  <br/> |
   
### <a name="class-identifiers"></a>Klassenbezeichner

```cpp
// {4e3a7680-b77a-11d0-9da5-00c04fd65685}
DEFINE_GUID(CLSID_IConverterSession, 0x4e3a7680, 0xb77a, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

### <a name="interface-identifiers"></a>Schnittstellenbezeichner

```cpp
// {4b401570-b77b-11d0-9da5-00c04fd65685}
DEFINE_GUID(IID_IConverterSession, 0x4b401570, 0xb77b, 0x11d0, 0x9d, 0xa5, 0x0, 0xc0, 0x4f, 0xd6, 0x56, 0x85);
```

## <a name="offline-state-api"></a>Offlinestatus-API

Dieser Abschnitt enthält Konstantendefinitionen und Klassen- und Schnittstellenbezeichner für die Offlinestatus-API.
  
### <a name="constants"></a>Konstanten

|||
|:-----|:-----|
|E_INVALIDARG  <br/> | *Wie in der Microsoft Windows Software Development Kit (SDK)-Headerdatei winerror.h definiert*  <br/> |
|E_NOINTERFACE  <br/> | *Wie in der Windows (SDK)-Headerdatei winerror.h definiert*  <br/> |
|MAPIOFFLINE_ADVISE_DEFAULT  <br/> |(ULONG)0  <br/> |
|MAPIOFFLINE_UNADVISE_DEFAULT  <br/> |(ULONG)0  <br/> |
|MAPIOFFLINE_ADVISE_TYPE_STATECHANGE  <br/> |1  <br/> |
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |0x1  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |0x2  <br/> |
|MAPIOFFLINE_FLAG_BLOCK  <br/> |0x00002000  <br/> |
|MAPIOFFLINE_FLAG_DEFAULT  <br/> |0x00000000  <br/> |
|MAPIOFFLINE_STATE_ALL  <br/> |0x003f037f  <br/> |
|**Online oder offline** <br/> ||
|MAPIOFFLINE_STATE_OFFLINE_MASK  <br/> |0x00000003  <br/> |
|MAPIOFFLINE_STATE_OFFLINE  <br/> |0x00000001  <br/> |
|MAPIOFFLINE_STATE_ONLINE  <br/> |0x00000002  <br/> |
   
### <a name="class-identifiers"></a>Klassenbezeichner

```cpp
//{fbeffd93-b11f-4094-842b-96dcd31e63d1}
DEFINE_GUID(GUID_GlobalState, 0xfbeffd93, 0xb11f, 0x4094, 0x84, 0x2b, 0x96, 0xdc, 0xd3, 0x1e, 0x63, 0xd1);
```

### <a name="interface-identifiers"></a>Schnittstellenbezeichner

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

Dieser Abschnitt enthält Konstantendefinitionen für benannte Eigenschaften und deren Namespaces sowie andere verwandte Konstanten.
  
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

### <a name="definitions-for-namespaces"></a>Definitionen für Namespaces

Die folgenden Globally Unique Identifiers (GUIDs) repräsentieren die Namespaces der benannten Eigenschaften.
  
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

Die PSETID-Definitionen finden Sie im Abschnitt MAPI-Speicher.
  
### <a name="other-constants"></a>Andere Konstanten

|||
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0xD000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x2000000  <br/> |
|MNID_ID  <br/> | *Wie in der Headerdatei mapidefs.h definiert.*  <br/> |
|MNID_STRING  <br/> | *Wie in der Headerdatei mapidefs.h definiert.*  <br/> |
|mtgNone  <br/> |0x0  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |
|mtgFullUpdate  <br/> |0x00010000  <br/> |
|mtgInfoUpdate  <br/> |0x00020000  <br/> |
|mtgOutofDate  <br/> |0x00080000  <br/> |
|mtgDelegated  <br/> |0x00100000  <br/> |
   
## <a name="replication-api"></a>Replikations-API

Dieser Abschnitt enthält die Konstantendefinitionen, MAPI-Schnittstellendeklarationen und Klassen- und Schnittstellenbezeichner für die Replikations-API.
  
### <a name="constants"></a>Konstanten

Im folgenden finden Sie eine [MAPIUID](mapiuid.md)-Struktur für die Identifizierung eines MAPI-Dienstanbieters: 
  
```cpp
const MAPIUID g_muidProvPrvNST = 
 { 0xE9, 0x2F, 0xEB, 0x75, 0x96, 0x50, 0x44, 0x86, 
      0x83, 0xB8, 0x7D, 0xE5, 0x22, 0xAA, 0x49, 0x48 };
```

|||
|:-----|:-----|
|DNH_OK  <br/> |0x00010000  <br/> |
|DNT_OK  <br/> |0x00010000  <br/> |
|HSF_LOCAL  <br/> |0x00000008  <br/> |
|HSF_COPYDESTRUCTIVE  <br/> |0x00000010  <br/> |
|HSF_OK  <br/> |0x00010000  <br/> |
|MDB_OST_LOGON_UNICODE  <br/> |((ULONG) 0x00000800)  <br/> |
|MDB_OST_LOGON_ANSI  <br/> |((ULONG) 0x00001000)  <br/> |
|SHOW_SOFT_DELETES  <br/> |((ULONG) 0x00000002)  <br/> |
|SS_ACTIVE  <br/> |0  <br/> |
|SS_SUSPENDED  <br/> |1  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |
|SYNC_BACKGROUND  <br/> |0x00001000  <br/> |
|SYNC_THESE_FOLDERS  <br/> |0x00020000  <br/> |
|SYNC_HEADERS  <br/> |0x02000000  <br/> |
|UPC_OK  <br/> |0x00010000  <br/> |
|UPD_ASSOC  <br/> |0x00000001  <br/> |
|UPD_MOV  <br/> |0x00000002  <br/> |
|UPD_OK  <br/> |0x00010000  <br/> |
|UPD_MOVED  <br/> |0x00020000  <br/> |
|UPD_UPDATE  <br/> |0x00040000  <br/> |
|UPD_COMMIT  <br/> |0x00080000  <br/> |
|UPF_NEW  <br/> |0x00000001  <br/> |
|UPF_MOD_PARENT  <br/> |0x00000002  <br/> |
|UPF_MOD_PROPS  <br/> |0x00000004  <br/> |
|UPF_DEL  <br/> |0x00000008  <br/> |
|UPF_OK  <br/> |0x00010000  <br/> |
|UPH_OK  <br/> |0x00010000  <br/> |
|UPM_ASSOC  <br/> |0x00000001  <br/> |
|UPM_NEW  <br/> |0x00000002  <br/> |
|UPM_MOV  <br/> |0x00000004  <br/> |
|UPM_MOD_PROPS  <br/> |0x00000008  <br/> |
|UPM_HEADER  <br/> |0x00000010  <br/> |
|UPM_OK  <br/> |0x00010000  <br/> |
|UPM_MOVED  <br/> |0x00020000  <br/> |
|UPM_COMMIT  <br/> |0x00040000  <br/> |
|UPM_DELETE  <br/> |0x00080000  <br/> |
|UPM_SAVE  <br/> |0x00100000  <br/> |
|UPR_ASSOC  <br/> |0x00000001  <br/> |
|UPR_READ  <br/> |0x00000002  <br/> |
|UPR_OK  <br/> |0x00010000  <br/> |
|UPR_COMMIT  <br/> |0x00020000  <br/> |
|UPS_UPLOAD_ONLY  <br/> |0x00000001  <br/> |
|UPS_DNLOAD_ONLY  <br/> |0x00000002  <br/> |
|UPS_ONE_FOLDER  <br/> |0x00000004  <br/> |
|UPS_THESE_FOLDERS  <br/> |0x00000080  <br/> |
|UPS_OK  <br/> |0x00010000  <br/> |
|UPT_OK  <br/> |0x00010000  <br/> |
|UPT_PUBLIC  <br/> |0x00000001  <br/> |
|UPV_ERROR  <br/> |0x00010000  <br/> |
|UPV_DIRTY  <br/> |0x00020000  <br/> |
|UPV_COMMIT  <br/> |0x00040000  <br/> |
   
### <a name="interface-declarations"></a>Schnittstellendeklarationen

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportHierarchyChanges,PXIHC);
```

```cpp
DECLARE_MAPI_INTERFACE_PTR(IExchangeImportContentsChanges,PXICC);
```

### <a name="interface-identifiers"></a>Schnittstellenbezeichner

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

Verwenden Sie die beiden folgenden Schnittstellenbezeichner [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md) oder [IMsgStore::OpenEntry](imsgstore-openentry.md), um alle Anbieterprüfungen bei einem Ordner- und einem Nachrichtenobjekt  zu öffnen und ignorieren. 
  
```cpp
//{57D333A0-F589-4b23-A3F9-85F82FEC153C}
DEFINE_GUID (IID_IMAPIFolderNoProvChk, 0x57D333A0, 0xF589, 0x4b23, 0xA3, 0xF9, 0x85, 0xF8, 0x2F, 0xEC, 0x15, 0x3C)
```

```cpp
//{C3505457-7B2E-4c3b-A8D6-6DD949BB97A1}
DEFINE_GUID (IID_IMessageNoProvChk, 0xC3505457, 0x7B2E, 0x4c3b, 0xA8, 0xD6, 0x6D, 0xD9, 0x49, 0xBB, 0x97, 0xA1)
```

## <a name="mapi-store"></a>MAPI-Speicher

Dieser Abschnitt enthält Konstantendefinitionen und Schnittstellenbezeichner, die von APIs mit einer MAPI-Speicher-Schnittstelle verwendet werden.
  
### <a name="constants"></a>Konstanten

||||
|:-----|:-----|:-----|
|fnevIndexing  <br/> |((ULONG) 0x00010000)  <br/> |Ein Speicheranbieter kann **FnevIndexing** im **UlEventType**-Mitglied der Struktur **[NOTIFICATION](notification.md)** bereitstellen, um den Indexer zu benachrichtigen, dass ein Objekt für die Indizierung bereitsteht. Das **info**-Mitglied der **NOTIFICATION**-Struktur enthält eine **[EXTENDED_NOTIFICATION](extended_notification.md)**-Struktur.  <br/> |
|FS_NONE  <br/> |0x00  <br/> |Ein Client kann **[IFolderSupport::GetSupportMask](ifoldersupport-getsupportmask.md)** aufrufen und die zurückgegebene Bitmaske überprüfen. **FS_NONE** gibt an, dass der Ordner keine Freigabe unterstützt.  <br/> |
|FS_SUPPORTS_SHARING  <br/> |0x01  <br/> |Ein Client kann **IFolderSupport::GetSupportMask** aufrufen und die zurückgegebene Bitmaske überprüfen. **FS_SUPPORTS_SHARING** gibt an, dass der Ordner die Freigabe unterstützt.  <br/> |
|INDEXING_SEARCH_OWNER  <br/> |((ULONG) 0x00000001)  <br/> |Gibt den Prozess an, bei dem eine Benachrichtigung an einen Indexer erfolgt, dass ein Objekt für die Indizierung bereit ist.  <br/> |
|MNID_ID  <br/> |Wie in der Microsoft Windows Software Development Kit (SDK)-Headerdatei mapidefs.h definiert  <br/> |Einen Wert für das **ulKind**-Feld der **[MAPINAMEID](mapinameid.md)**-Struktur.  <br/> |
|MNID_STRING  <br/> |Wie in der Microsoft Windows Software Development Kit (SDK)-Headerdatei mapidefs.h definiert.  <br/> |Einen Wert für das **ulKind**-Feld der **[MAPINAMEID](mapinameid.md)**-Struktur.  <br/> |
|MSCAP_RES_ANNOTATION  <br/> |((ULONG) 0x00000001)  <br/> |Wenn ein Client **MSCAP_SEL_RESTRICTION** im *MscapSelector* für **[IMSCapabilities::GetCapabilities](imscapabilities-getcapabilities.md)** angibt, kann **GetCapabilities** diesen Wert zurückzugeben, wenn der Speicher ungültige Parameter in einer Einschränkung ignoriert.  <br/> |
|MSCAP_SECURE_FOLDER_HOMEPAGES  <br/> |((ULONG) 0x00000020)  <br/> |Wenn ein Client **MSCAP_SEL_FOLDER** im *MscapSelector* für **IMSCapabilities::GetCapabilities** angibt, kann **GetCapabilities** diesen Wert zurückzugeben, wenn es sich bei dem Speicher um einen nicht standardmäßigen Speicher handelt, der Ordnerhomepages unterstützt.   <br/> |
|STORE_PUSHER_OK  <br/> |((ULONG) 0x00800000)  <br/> |Ein Client kann die Eigenschaft **[PR_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)** abrufen, um das Merkmal eines Nachrichtenspeichers zu ermitteln. Wenn der Speicheranbieter die **STORE_PUSHER_OK**-Kennzeichnung in die Bitmaske einfügt, bedeutet dies, dass der MAPI-Protokollhandler den Speicher nicht durchforstet und der Speicher alle Benachrichtigungen über Änderungen an den Indexer senden muss, damit die Nachrichten indiziert werden.  <br/> |
   
### <a name="definitions-for-namespaces"></a>Definitionen für Namespaces

Die folgenden Globally Unique Identifiers (GUIDs) repräsentieren die Namespaces benannter Eigenschaften. Sie werden durch den MAPI Protocol Handler (PH) indiziert und als schreibgeschützt dokumentiert.
  
> [!CAUTION]
> Die benannten Eigenschaften sollte nicht zum Erstellen oder Ändern von Elementen verwendet werden. 
  
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

### <a name="interface-identifiers"></a>Schnittstellenbezeichner

```cpp
//{00375ac3-ecaf-4ef8-a527-34f452fa9c67}
DEFINE_GUID(IID_IFolderSupport, 0x00375ac3, 0xecaf, 0x4ef8, 0xa5, 0x27, 0x34, 0xf4, 0x52, 0xfa, 0x9c, 0x67);

```

```cpp
//{29F3AB10-554d-11d0-a97c-00a0c911f50a}
#define DEFINE_PRXGUID(_name, _l) DEFINE_GUID(_name, (0x29f3ab10 + _l), 0x554d, 0x11d0, 0xa9, 0x7c, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x0a) 
DEFINE_PRXGUID(IID_IProxyStoreObject, 0x00000000L);
```

Verwenden Sie das in der Windows SDK-Headerdatei guiddef.h definierte `DEFINE_OLEGUID`-Makro, um den folgenden symbolischen GUID-Namen seinem Wert zuzuordnen. 
  
```cpp
//{00020393-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_IMSCapabilities, 0x00020393, 0, 0)

```

## <a name="mapi-address-book-constants"></a>MAPI-Adressbuch-Konstanten

Dieser Abschnitt enthält Definitionen für das MAPI-Adressbuch.
  
### <a name="constants"></a>Konstanten

||||
|:-----|:-----|:-----|
|CONTAB_ROOT  <br/> |((ULONG) 0x00000001)  <br/> |Der Stammordner für ein MAPI-Adressbuch-Objekt.  <br/> |
|CONTAB_SUBROOT  <br/> |((ULONG) 0x00000002)  <br/> |Ein im Stammordner des MAPI-Adressbuch-Objekts enthaltener Unterordner.  <br/> |
|CONTAB_CONTAINER  <br/> |((ULONG) 0x00000003)  <br/> |Ein Adressbuchcontainer-Objekt.  <br/> |
|CONTAB_USER  <br/> |((ULONG) 0x00000004)  <br/> |Ein Nachrichtenbenutzer-Objekt.  <br/> |
|CONTAB_DISTLIST  <br/> |((ULONG) 0x00000005)  <br/> |Ein Verteilerliste-Objekte.  <br/> |
   
## <a name="additional-mapi-constants"></a>Zusätzliche MAPI-Konstanten

Dieser Abschnitt enthält Konstantendefinitionen, einschließlich Fehlercodes, und Schnittstellenbezeichner, die von MAPI-APIs verwendet werden, die zuvor nicht verfügbar gemacht und dokumentiert wurden.
  
||||
|:-----|:-----|:-----|
|DIALOG_MODAL  <br/> |((ULONG) 0x00000001)  <br/> |Wenn ein Client die [IAddrBook::Details](iaddrbook-details.md)-Methode aufruft, muss der Client die **DIALOG_MODAL**-Kennzeichnung im _UlFlags_-Parameter festlegen, um das modale Dialogfeld mit Details zu einem bestimmten Adressbucheintrag anzuzeigen. Diese Konstante wird in mapidefs.h definiert.  <br/> |
|ITEMPROC_FORCE  <br/> |0x00000800  <br/> |In Outlook 2007 wenden umschlossene PST-Speicher Regeln und Spamfilter auf neue Nachrichten an, bevor MAPI-Clients über die neuen Nachrichten informiert werden. Ein Anbieter oder Client, der die [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)-Methode verwendet, um eine neue Nachricht in PST-Speichern zu erstellen, sollte die **ITEMPROC_FORCE**-Kennzeichnung im _UlFlags_-Parameter der [IMAPIProp::SaveChanges](imapiprop-savechanges.md)-Methode festlegen, um dem PST-Speicher mitzuteilen, dass die Nachricht zur Regelverarbeitung berechtigt ist, bevor der Speicher einen überwachenden Client über die Ankunft der Nachricht informiert. Beachten Sie, dass diese Regelverarbeitung sich nur auf neue, auf einem anderen als einem Microsoft Exchange Server erstellte Nachrichten bezieht, da Exchange-Server Regeln für Nachrichten auf dem Server verarbeitet. Der Anbieter oder Client, der die Nachricht erstellt, muss diese Kennzeichnung zusammen mit **NON_EMS_XP_SAVE** übergeben, um anzugeben, dass es sich nicht um einen Exchange-Server handelt.  <br/> |
| MAPI_BG_SESSION  <br/> |0x00200000  <br/> |Ein Client kann die [MAPILogonEx](mapilogonex.md)-Funktion aufrufen und die **MAPI_BG_SESSION**-Kennzeichnung im _flFlags_-Parameter einstellen, um sich bei einer Sitzung anzumelden und alle Vorgänge im Hintergrund auszuführen. Wenn ein Client eine Verarbeitung in einem Hintergrund-Thread oder separaten Prozess in einer Weise plant, die den Thread im Vordergrund nicht stört, sollte [MAPILogonEx](mapilogonex.md) mit der **MAPI_BG_SESSION**-Kennzeichnung aufgerufen werden. Dies ist beispielsweise bei einer Clientanwendung wie der Indizierungs-Engine der Fall, bei der eine Persönliche Ordner-Datei (PST) für den Zugriff im Hintergrund geöffnet wird.  <br/> |
|MAPI_CACHE_ONLY  <br/> |0x00004000  <br/> |Ein Client kann die [IAddrBook::OpenEntry](iaddrbook-openentry.md)-Methode aufrufen und die **MAPI_CACHE_ONLY**-Kennzeichnung im _ulFlags_-Parameter festlegen, um einen Adressbucheintrag zu öffnen und ausschließlich aus dem Cache darauf zuzugreifen. Ein Beispiel für diese Anwendung ist eine Clientanwendung, mit der die globale Adressliste im Exchange-Cache-Modus geöffnet und aus dem Cache auf einen Eintrag in diesem Adressbuch zugegriffen werden soll, ohne Datenverkehr zwischen dem Client und dem Server zu verursachen.  <br/> |
|MAPI_DIALOG_MODELESS  <br/> |0x0000000C  <br/> |Dieser Wert kann an die MAPISendMail-Funktion von Simple MAPI im _ulFlags_-Parameter übergeben werden, um anzugeben, dass ein nicht modales Dialogfeld von der standardmäßigen E-Mail-Anwendung angezeigt wird. Wenn weder diese Kennzeichnung noch MAPI_DIALOG (0 x 00000008) festgelegt wird, wird das Dialogfeld nicht angezeigt.  <br/> |
|MAPI_NO_CACHE  <br/> |0x00000200  <br/> |Wenn sich Microsoft Office Outlook im Exchange-Cache-Modus befindet und der Speicher im Cache-Modus geöffnet wurde, kann ein Client oder Dienstanbieter [IMsgStore::OpenEntry](imsgstore-openentry.md) aufrufen und die **MAPI_NO_CACHE**-Kennzeichnung im _ulFlags_-Parameter festlegen, um ein Element oder einen Ordner auf dem Remotespeicher zu öffnen. Hinweise: Wenn Sie den Nachrichtenspeicher mit der **MDB_ONLINE**-Kennzeichnung auf dem Remoteserver öffnen, brauchen Sie die **MAPI_NO_CACHE**-Kennzeichnung nicht zu verwenden.  <br/> |
|MAPI_UNICODE  <br/> |0x80000000  <br/> |Ein Client oder Dienstanbieter kann die [OpenIMsgOnIStg](openimsgonistg.md)-Funktion aufrufen und die **MAPI_UNICODE**-Kennzeichnung im _ulFlags_-Parameter einstellen, um  Unicode-MSG-Dateien zu erstellen. Die sich daraus ergebende [IMessage: IMAPIProp](imessageimapiprop.md)-Datei zeigt **STORE_UNICODE_OK** in der [kanonischen Eigenschaft PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) an und unterstützt Unicode-Eigenschaften. Diese Konstante wird in mapidefs.h definiert.  <br/> |
|MDB_ONLINE  <br/> |0x00000100  <br/> |Wenn sich Outlook im Exchange-Cache-Modus befindet, kann ein Client oder Dienstanbieter die [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)-Methode aufrufen und die **MDB_ONLINE**-Kennzeichnung im _ulFlags_-Parameter festlegen, um die Verbindung mit dem lokalen Nachrichtenspeicher zu überschreiben und den Speicher auf dem Remoteserver zu öffnen. Beachten Sie, dass Sie einen Exchange-Speicher innerhalb der gleichen MAPI-Sitzung nicht gleichzeitig im Cache-Modus und im Nicht-Cache-Modus öffnen können. Wenn Sie den zwischengespeicherten Nachrichtenspeicher bereits geöffnet haben, müssen Sie entweder den Speicher schließen, bevor Sie ihn mit dieser Kennzeichnung öffnen, oder eine neue MAPI-Sitzung öffnen, in der Sie den Exchange-Speicher auf dem Remoteserver mit dieser Kennzeichnung öffnen können.  <br/> |
|NON_EMS_XP_SAVE  <br/> |0x00001000  <br/> |Ein Client kann die [IMAPIProp::SaveChanges](imapiprop-savechanges.md)-Methode mit der **NON_EMS_XP_SAVE**-Kennzeichnung im _ulFlags_-Parameter festlegen, um anzugeben, dass die Nachricht nicht von einem Exchange-Server gesendet wurde. Diese Kennzeichnung sollt in Verbindung mit der **ITEMPROC_FORCE**-Kennzeichnung im _ulFlags_-Parameter verwendet werden, um einen PST-Speicher darauf hinzuweisen, dass die Nachricht für die Regelverarbeitung berechtigt ist, bevor der PST-Speicher einen überwachenden Client über die Ankunft der Nachricht informiert. Diese Regelverarbeitung gilt nur für neue Nachrichten, die mit [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) auf einem anderen Server als dem Exchange-Server erstellt wurden (da der Exchange-Server bereits die Regelverarbeitung vorgenommen hätte).  <br/> |
|SPAMFILTER_ONSAVE  <br/> |0x00000080  <br/> |Ein Client kann [IMAPIProp::SaveChanges](imapiprop-savechanges.md) aufrufen und die **SPAMFILTER_ONSAVE**-Kennzeichnung im _ulFlags_-Parameter festlegen, um einen Spamfilter auf die gespeicherte Nachricht anzuwenden. Spamfilter-Unterstützung ist nur verfügbar, wenn der E-Mail-Adressentyp des Absenders Simple Mail Transfer Protocol (SMTP) ist und die Nachricht auf einem Speicher für eine Persönliche Ordner-Datei (PST) gespeichert wird.  <br/> |
|STORE_ITEMPROC  <br/> |0x00200000  <br/> |Wenn diese Kennzeichnung in der [kanonischen Eigenschaft PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) eines umschlossenen PST-Speichers festgelegt wird, bedeutet dies, dass der Speicher beim Eintreffen einer neuen Nachricht Regeln und Spamfilter auf die Nachricht anwendet. Anschließend ruft der Speicher [IMAPISupport::Notify](imapisupport-notify.md) auf und legt **FnevNewMail** in der [NOTIFICATION](notification.md)-Struktur fest, was als Parameter übergeben wird. Die Details der neuen Nachricht werden an einen überwachenden Client weitergegeben. Wenn der überwachende Client die Nachricht erhält, wendet er keine Regeln darauf an.  <br/> |
|STORE_UNICODE_OK  <br/> |0x00040000  <br/> |Wenn diese Kennzeichnung in der [kanonischen Eigenschaft PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md) enthalten ist, bedeutet dies, dass der Speicher Unicode-Speicherung unterstützt. Ein Client kann das Vorhandensein dieser Kennzeichnung überprüfen und entscheiden, ob er Unicode-Informationen abruft oder speichert.  <br/> |
   
### <a name="definitions-for-archiving-items-in-a-folder"></a>Definitionen zum Archivieren von Elementen in einem Ordner

Die folgenden Konstantendefinitionen sind Werte, die verwendet werden, um die [kanonische Eigenschaft PidTagAgingGranularity](pidtagaginggranularity-canonical-property.md) festzulegen.
  
```cpp
#define AG_MONTHS 0 
#define AG_WEEKS  1 
#define AG_DAYS   2 

```

### <a name="definitions-for-displaying-remote-objects"></a>Definitionen zum Anzeigen von Remoteobjekten

Die folgenden Konstanten- und Makrodefinitionen dienen zum Anzeigen von Remoteobjekten. Weitere Informationen finden Sie unter [Kanonische Eigenschaft PidTagDisplayTypeEx](pidtagdisplaytypeex-canonical-property.md).
  
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

### <a name="definitions-for-exchange-address-book-and-message-store-error-codes"></a>Definitionen für Exchange-Adressbuch- und Message Store-Fehlercodes

Nachfolgend finden Sie Fehlercode-Definitionen für das Exchange-Adressbuch und Message Store, die über eine Verbindungswiederherstellungsfunktion verfügen. Der letzte Aufruf an einen nicht verbundenen Global Catalog (GC) kann zu einem **MAPI_E_END_OF_SESSION**-Fehler führen, sodass eine Wiederherstellung der Verbindung erforderlich ist. 
  
Outlook-MAPI unterstützt die erneute Verbindung mit einem globalen Katalogserver, ohne dass eine spezielle Neukonfiguration erforderlich ist, aber es können andere Fehlercodes an den Client zurückgegeben werden.
  
||||
|:-----|:-----|:-----|
|MAPI_E_END_OF_SESSION  <br/> |0x80040200  <br/> |Wird zurückgegeben, wenn eine Verbindung getrennt wurde.  <br/> |
|MAPI_E_RECONNECTED  <br/> |0x80040125  <br/> |Wird zurückgegeben, wenn das Verbindungstoken Remote Procedure Call (RPC) nicht mehr aktuell ist. Wenn das Token der aktuellen Transaktion vom Token der Verbindung abweicht, bedeutet dies, dass die Verbindung unterbrochen wurde. **MAPI_E_RECONNECTED** wird zurückgegeben und kann auf die gleiche Weise wie **MAPI_E_END_OF_SESSION** behoben werden. Der Aufruf sollte wiederholt werden.  <br/> |
|MAPI_E_OFFLINE  <br/> |0x80040126  <br/> |Wird zurückgegeben, wenn die Verbindung offline ist. In der Regel bedeutet dies, dass sich etwas in der Umgebung ereignet hat, z. B. ein Serverfehler oder den Verlust der Netzwerkkonnektivität. Dieser Fehler tritt meistens auf, wenn Sie ein Cache-Modus-Profil verwenden und versuchen, den Cache für die Kommunikation mit dem Server zu umgehen. Wenn der Cache nie in der Lage war, eine Verbindung zum Server herzustellen, kann er sich im Status "offline" befinden, sodass **MAPI_E_OFFLINE** ausgegeben werden kann.  <br/> |
   
Keiner der beiden vorherigen Fehler wird in Szenarien zurückgegeben, in denen sie normalerweise auftreten würden. In den meisten Fällen wird **MAPI\_E_NETWORK_ERROR** oder **MAPI_E_CALL_FAILED** zurückgegeben. Keiner tritt bei der Verwendung des Downloads [Microsoft Exchange Server MAPI Client and Collaboration Data Objects 1.2.1](http://support.microsoft.com/kb/171440) auf. 
  
### <a name="definitions-for-exchange-server-mailbox-cached-mode-quotas"></a>Definitionen für Exchange Server-Postfach-Cache-Modus-Kontingente

Die folgenden Konstantendefinitionen werden von Microsoft Outlook 2010 und Microsoft Outlook 2013 verwendet, um die Exchange-Cache-Modus-Profilkontingente festzulegen, die den Exchange-Postfachkontingenten entsprechen und andernfalls nur mit einem Online-Profil verfügbar sind.
  
```cpp
#define PR_QUOTA_WARNING PROP_TAG( PT_LONG, 0x341A)
#define PR_QUOTA_SEND    PROP_TAG( PT_LONG, 0x341B)
#define PR_QUOTA_RECEIVE PROP_TAG( PT_LONG, 0x341C)
```

Diese Eigenschaften sind den entsprechenden Online-Eigenschaften zugeordnet und enthalten dieselben Werte in Kilobyte. PR_QUOTA_WARNING entspricht PR_STORAGE_QUOTA_LIMIT, PR_QUOTA_SEND entspricht PR_QUOTA_PROHIBIT_SEND_QUOTA und PR_QUOTA_RECEIVE entspricht PR_PROHIBIT_RECEIVE_QUOTA.
  
### <a name="definitions-for-message-format"></a>Definitionen für Nachrichtenformat

Die folgenden Konstantendefinitionen sind Werte, die verwendet werden, um die [kanonische Eigenschaft PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md) festzulegen.
  
```cpp
#define EDITOR_FORMAT_DONTKNOW  ((ULONG) 0) 
#define EDITOR_FORMAT_PLAINTEXT ((ULONG) 1) 
#define EDITOR_FORMAT_HTML      ((ULONG) 2) 
#define EDITOR_FORMAT_RTF       ((ULONG) 3)
```

### <a name="definitions-for-using-rpc-over-http"></a>Definitionen für die Verwendung von RPC über HTTP

Unter [kanonische Eigenschaft PidTagRpcOverHttpFlags](pidtagrpcoverhttpflags-canonical-property.md) finden Sie Konstantendefinitionen, die als Kennzeichnungen zum Festlegen der Eigenschaft verwendet werden. 
  
Unter [kanonische Eigenschaft PidTagRpcOverHttpProxyAuthScheme](pidtagrpcoverhttpproxyauthscheme-canonical-property.md) finden Sie Konstantendefinitionen, die zum Festlegen der Eigenschaft verwendet werden. 
  
### <a name="identifiers"></a>Bezeichner

Verwenden Sie das in der Microsoft Windows Software Development Kit (SDK)-Headerdatei guiddef.h definierte `DEFINE_OLEGUID`-Makro, um die folgenden symbolischen GUID-Namen (Globally Unique Identifier) Ihren Werten zuzuordnen. 
  
```cpp
//{0002038A-0000-0000-C000-000000000046}
#if !defined(INITGUID) || defined(USES_IID_IMessageRaw) 
DEFINE_OLEGUID(IID_IMessageRaw,0x0002038A, 0, 0); 
#endif
```

Der folgende Bezeichner gilt für den Abschnitt Capone-Profil eines Adressbuchs, der zur Unterstützung mehrerer ([MultiEx](using-multiple-exchange-accounts.md))-Postfächer eine [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)-Eigenschaft enthält, die effektiv den von [SetDefaultDir](iaddrbook-setdefaultdir.md) angegebenen standardmäßigen Container deaktiviert.
  
```cpp
// {00020D0A-0000-0000-C000-000000000046}
DEFINE_OLEGUID(IID_CAPONE_PROF, 0x00020d0a, 0, 0);
```

### <a name="interface-identifiers"></a>Schnittstellenbezeichner

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

### <a name="pst-override-handler-interface-identifiers"></a>Schnittstellenbezeichner für PST-Override-Handler

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
- [Zugreifen auf einen Speicher auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)
- [Öffnen eines Speichers auf dem Remoteserver, wenn Outlook sich im Exchange-Cache-Modus befindet](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [Verwalten einer Nachricht in einem OST ohne Aufrufen einer Synchronisierung im Exchange-Cache-Modus](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

