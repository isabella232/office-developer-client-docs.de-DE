---
title: Algorithmus für die Berechnung der Anzahl der Store Hash
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 489e0d74-8ecd-23ba-c874-18fd8c50fd12
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: de4fa7cb24cd486e506f5d747319c44ce9c15a77
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791277"
---
# <a name="algorithm-to-calculate-the-store-hash-number"></a><span data-ttu-id="44614-103">Algorithmus für die Berechnung der Anzahl der Store Hash</span><span class="sxs-lookup"><span data-stu-id="44614-103">Algorithm to Calculate the Store Hash Number</span></span>
 
<span data-ttu-id="44614-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44614-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44614-105">Im Rahmen einer MAPI-Uniform Resource Locator (URL) sendet ein Anbieter anmelden eine Store Hash Zahl an der MAPI-Protokollhandler, um ein Objekt zu identifizieren, die für die Indizierung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="44614-105">As part of a MAPI Uniform Resource Locator (URL), a store provider sends a store hash number to the MAPI Protocol Handler to identify an object that is ready for indexing.</span></span> <span data-ttu-id="44614-106">Der MAPI-Protokollhandler verwendet diese Store Hash-Nummer zum Identifizieren eines Speichers an.</span><span class="sxs-lookup"><span data-stu-id="44614-106">The MAPI Protocol Handler uses this store hash number to identify a store.</span></span> <span data-ttu-id="44614-107">Im Allgemeinen berechnet ein Anbieter anmelden die Store Hash-Nummer auf der Grundlage der Store Zuordnung Signatur, wenn der Informationsspeicher die **[PR_MAPPING_SIGNATURE](pidtagmappingsignature-canonical-property.md)** -Eigenschaft im Abschnitt globale Profile definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="44614-107">In general, a store provider calculates the store hash number based on the store mapping signature, if the store has the **[PR_MAPPING_SIGNATURE](pidtagmappingsignature-canonical-property.md)** property defined in the global profile section.</span></span> <span data-ttu-id="44614-108">Andernfalls wird die Store-Eintrags-ID verwendet Speicheranbieter</span><span class="sxs-lookup"><span data-stu-id="44614-108">Otherwise, the store provider uses the store entry ID.</span></span> <span data-ttu-id="44614-109">Der Algorithmus zum Berechnen der Anzahl der Store Hash muss Mehrdeutigkeiten identifizieren Speicher minimieren.</span><span class="sxs-lookup"><span data-stu-id="44614-109">The algorithm to calculate the store hash number must minimize ambiguities identifying stores.</span></span> 
  
<span data-ttu-id="44614-110">In diesem Thema wird einem Algorithmus, Microsoft Office Outlook eine Store Hash Zahl berechnet auf die Speicher Zuordnung Signatur- oder Eintrags-ID und der Dateiname für den Basis.</span><span class="sxs-lookup"><span data-stu-id="44614-110">This topic describes an algorithm that Microsoft Office Outlook uses to calculate a store hash number based on the store mapping signature or entry ID and the store file name.</span></span> 
  
<span data-ttu-id="44614-111">Das binäre Blob zu codierenden ist die PR_ENTRYID des Speichers in den meisten Fällen, aber für zwischengespeicherte Exchange-Speicher, öffentliche und Private, die binäre Blob der PR_MAPPING_SIGNATURE sollte, im Profil vorhanden.</span><span class="sxs-lookup"><span data-stu-id="44614-111">The binary blob to be encoded is the PR_ENTRYID of the store in most cases, but for cached Exchange stores, both public and private, the binary blob should be the PR_MAPPING_SIGNATURE, found in the profile.</span></span>
  
<span data-ttu-id="44614-112">Nach dem computing Hash für BLOBs für einen Informationsspeicher für Öffentliche Ordner, jedoch vor hashing in der OST-Pfad die Konstante 0x2E505542, die die Zeichenfolge darstellt ". PUB", ist in Hash, um sicherzustellen, ist eindeutig, d. h., getrennt von den privaten Speicher Hash.</span><span class="sxs-lookup"><span data-stu-id="44614-112">After computing the hash for a public folder store's binary blob, but before hashing-in the OST path, the constant 0x2E505542, which represents the string ".PUB", is hashed in to assure it is unique, that is, distinct from the private store's hash.</span></span>
  
<span data-ttu-id="44614-113">Der Support-Code culls die relevanten Bits aus dem Profil, die verwendet werden kann, um festzustellen, ob ein Speicher wird öffentliche oder private, wenn es zwischengespeichert wird, und den Pfad zu der OST.</span><span class="sxs-lookup"><span data-stu-id="44614-113">The support code culls the relevant bits from the profile, which can be used to determine whether a store is public or private, if it's cached, and the path to the OST.</span></span> <span data-ttu-id="44614-114">Um diesen Code in einem Projekt zu integrieren, rufen Sie die Funktion ComputeStoreHash, die als Eingabe den Sitzung Zeiger akzeptiert sowie PR\_ENTRYID, PR\_SERVICE_UID und PR\_MDB_PROVIDER aus der Nachricht speichern Tabelle.</span><span class="sxs-lookup"><span data-stu-id="44614-114">To incorporate this code in a project, call the function ComputeStoreHash, which takes as its input the session pointer as well as PR\_ENTRYID, PR\_SERVICE_UID, and PR\_MDB_PROVIDER from the message store table.</span></span> <span data-ttu-id="44614-115">Die restlichen die benötigten Informationen Es ruft aus dem Profil ab.</span><span class="sxs-lookup"><span data-stu-id="44614-115">The rest of the information it needs it gets from the profile.</span></span> <span data-ttu-id="44614-116">Für die Ausgabe, diese Funktion gibt den Hash, wie Sie anhand der PR berechnet\_MAPPING_SIGNATURE, wenn der Informationsspeicher zwischengespeicherten Exchange-Speicher oder den Hash ist, wie Sie anhand der PR berechnet\_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="44614-116">For output, this function returns the hash as computed from PR\_MAPPING_SIGNATURE if the store is a cached Exchange store, or the hash as computed from PR\_ENTRYID.</span></span>
  
> [!NOTE]
> <span data-ttu-id="44614-117">Die HrEmsmdbUIDFromStore Support-Funktion ist eine [Mehrerer Exchange-Konten](using-multiple-exchange-accounts.md)-unterstützende Ersatz für die Verwendung von PbGlobalProfileSectionGuid zum Profilabschnitt für ein Exchange-Postfach zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="44614-117">The HrEmsmdbUIDFromStore support function is a [Multiple Exchange Accounts](using-multiple-exchange-accounts.md)-aware replacement for using pbGlobalProfileSectionGuid to open the profile section for an Exchange mailbox.</span></span> 
  
```cpp
#define PR_PROFILE_OFFLINE_STORE_PATH_A PROP_TAG(PT_STRING8, 0x6610)
#define PR_PROFILE_OFFLINE_STORE_PATH_W PROP_TAG(PT_UNICODE, 0x6610)
#define CONFIG_OST_CACHE_PRIVATE  ((ULONG)0x00000180)
#define CONFIG_OST_CACHE_PUBLIC   ((ULONG)0x00000400)
HRESULT HrEmsmdbUIDFromStore(IMAPISession* pmsess,
                             MAPIUID* puidService,
                             MAPIUID* pEmsmdbUID)
{
  if (!puidService) return MAPI_E_INVALID_PARAMETER;
  HRESULT hRes = S_OK;
  SRestriction mres = {0};
  SPropValue mval = {0};
  SRowSet* pRows = NULL;
  SRow* pRow = NULL;
  LPSERVICEADMIN spSvcAdmin = NULL;
  LPMAPITABLE spmtab = NULL;
  enum { eEntryID = 0, eSectionUid, eMax };
  static const SizedSPropTagArray(eMax, tagaCols) =
  {
    eMax,
    {
      PR_ENTRYID,
      PR_EMSMDB_SECTION_UID,
    }
  };
  hRes = pmsess->AdminServices(0, (LPSERVICEADMIN*)&spSvcAdmin);
  if (SUCCEEDED(hRes) && spSvcAdmin)
  {
    hRes = spSvcAdmin->GetMsgServiceTable(0, &spmtab);
    if (spmtab)
    {
      hRes = spmtab->SetColumns((LPSPropTagArray)&tagaCols, TBL_BATCH);
      mres.rt = RES_PROPERTY;
      mres.res.resProperty.relop = RELOP_EQ;
      mres.res.resProperty.ulPropTag = PR_SERVICE_UID;
      mres.res.resProperty.lpProp = &mval;
      mval.ulPropTag = PR_SERVICE_UID;
      mval.Value.bin.cb = sizeof(*puidService);
      mval.Value.bin.lpb = (LPBYTE)puidService;
      (void) spmtab->Restrict(&mres, 0);
      (void) spmtab->QueryRows(10, 0, &pRows);
      if (SUCCEEDED(hRes) && pRows && pRows->cRows)
      {
        pRow = &pRows->aRow[0];
        if (pEmsmdbUID && pRow)
        {
          if (PR_EMSMDB_SECTION_UID == pRow->lpProps[eSectionUid].ulPropTag &&
            pRow->lpProps[eSectionUid].Value.bin.cb == sizeof(*pEmsmdbUID))
          {
            memcpy(pEmsmdbUID, pRow->lpProps[eSectionUid].Value.bin.lpb, sizeof(*pEmsmdbUID));
          }
        }
      }
      FreeProws(pRows);
    }
    if (spmtab) spmtab->Release();
  }
  if (spSvcAdmin) spSvcAdmin->Release();
  return hRes;
} // HrEmsmdbUIDFromStore
bool FExchangePrivateStore(LPMAPIUID lpmapiuid)
{
  if (!lpmapiuid) return false;
  return IsEqualMAPIUID(lpmapiuid, (LPMAPIUID)pbExchangeProviderPrimaryUserGuid);
} // FExchangePrivateStore
bool FExchangePublicStore(LPMAPIUID lpmapiuid)
{
  if (!lpmapiuid) return false;
  return IsEqualMAPIUID(lpmapiuid, (LPMAPIUID)pbExchangeProviderPublicGuid);
} // FExchangePublicStore
DWORD ComputeHash(ULONG cbStoreEID, LPBYTE pbStoreEID, LPCSTR pszFileName, LPCWSTR pwzFileName, BOOL bPublicStore)
{
  DWORD  dwHash = 0;
  ULONG  cdw    = 0;
  DWORD* pdw    = NULL;
  ULONG  cb     = 0;
  BYTE*  pb     = NULL;
  ULONG  i      = 0;
  if (!cbStoreEID || !pbStoreEID) return dwHash;
  // Shouldn't see both of these at the same time.
  if (pszFileName && pwzFileName) return dwHash;
  // Get the Store Entry ID
  // pbStoreEID is a pointer to the Entry ID.
  // cbStoreEID is the size in bytes of the Entry ID.
  pdw = (DWORD*)pbStoreEID;
  cdw = cbStoreEID / sizeof(DWORD);
  for (i = 0; i < cdw; i++)
  {
    dwHash = (dwHash << 5) + dwHash + *pdw++;
  }
  pb = (BYTE *)pdw;
  cb = cbStoreEID % sizeof(DWORD);
  for (i = 0; i < cb; i++)
  {
    dwHash = (dwHash << 5) + dwHash + *pb++;
  }
  if (bPublicStore)
  {
    // Augment to assure it is unique, else could be same as private store.
    dwHash = (dwHash << 5) + dwHash + 0x2E505542; // this is '.PUB'
  }
  // To also include the store file name in the hash calculation,
  // pszFileName and pwzFileName are NULL terminated strings with the path and filename of the store.
  if (pwzFileName)
  {
    while (*pwzFileName)
    {
      dwHash = (dwHash << 5) + dwHash + *pwzFileName++;
    }
  }
  else if (pszFileName)
  {
    while (*pszFileName)
    {
      dwHash = (dwHash << 5) + dwHash + *pszFileName++;
    }
  }
  // dwHash now contains the hash to be used. It should be written in hex when building a URL.
  return dwHash;
} // ComputeHash
void ComputeStoreHash(LPMAPISESSION lpMAPISession, LPSBinary lpEntryID, LPSBinary lpServiceUID, LPSBinary lpProviderUID, DWORD* lpdwSigHash, DWORD* lpdwEIDHash)
{
  HRESULT hRes = S_OK;
  MAPIUID emsmdbUID = {0};
  LPPROFSECT lpProfSect = NULL;
  BOOL fPublicExchangeStore  = FExchangePublicStore((LPMAPIUID)lpProviderUID->lpb);
  BOOL fPrivateExchangeStore = FExchangePrivateStore((LPMAPIUID)lpProviderUID->lpb);
  BOOL fCached = false;
  LPSPropValue lpConfigProp = NULL;
  LPSPropValue lpPathPropA = NULL;
  LPSPropValue lpPathPropW = NULL;
  LPSPropValue lpMappingSig = NULL;
  LPSTR szPath = NULL; // Do not free.
  LPWSTR wzPath = NULL; // Do not free.
  // Get profile section.
  if (lpServiceUID)
  {
    hRes = HrEmsmdbUIDFromStore(lpMAPISession,
      (LPMAPIUID) lpServiceUID->lpb,
      &emsmdbUID);
    if (SUCCEEDED(hRes))
    {
      hRes = lpMAPISession->OpenProfileSection(&emsmdbUID, NULL, 0, &lpProfSect);
    }
  }
  if (!lpServiceUID || FAILED(hRes))
  {
    // For Outlook 2003/2007, HrEmsmdbUIDFromStore may not succeed,
    // so use pbGlobalProfileSectionGuid instead.
    hRes = lpMAPISession->OpenProfileSection((LPMAPIUID)pbGlobalProfileSectionGuid, NULL, 0, &lpProfSect);
  }
  if (lpProfSect)
  {
    hRes = HrGetOneProp(lpProfSect, PR_PROFILE_CONFIG_FLAGS, &lpConfigProp);
    if (SUCCEEDED(hRes) && PROP_TYPE(lpConfigProp->ulPropTag) != PT_ERROR)
    {
      if (fPrivateExchangeStore)
      {
        fCached = ((lpConfigProp->Value.l & CONFIG_OST_CACHE_PRIVATE) != 0);
      }
      if (fPublicExchangeStore)
      {
        fCached = ((lpConfigProp->Value.l & CONFIG_OST_CACHE_PUBLIC) == CONFIG_OST_CACHE_PUBLIC);
      }
    }
    if (fCached)
    {
      hRes = HrGetOneProp(lpProfSect, PR_PROFILE_OFFLINE_STORE_PATH_W, &lpPathPropW);
      if (FAILED(hRes))
      {
        hRes = HrGetOneProp(lpProfSect, PR_PROFILE_OFFLINE_STORE_PATH_A, &lpPathPropA);
      }
      if (SUCCEEDED(hRes))
      {
        if (lpPathPropW && lpPathPropW->Value.lpszW)
        {
          wzPath = lpPathPropW->Value.lpszW;
        }
        else if (lpPathPropA && lpPathPropA->Value.lpszA)
        {
          szPath = lpPathPropA->Value.lpszA;
        }
      }
      // If this is an Exchange store with an OST path, it's an OST, so get the mapping signature.
      if ((fPrivateExchangeStore || fPublicExchangeStore) && (wzPath || szPath))
      {
        hRes = HrGetOneProp(lpProfSect, PR_MAPPING_SIGNATURE, &lpMappingSig);
      }
    }
  }
  DWORD dwSigHash = NULL;
  if (lpMappingSig && PT_BINARY == PROP_TYPE(lpMappingSig->ulPropTag))
  {
    dwSigHash = ComputeHash(lpMappingSig->Value.bin.cb, lpMappingSig->Value.bin.lpb, NULL, NULL, fPublicExchangeStore);
  }
  DWORD dwEIDHash = ComputeHash(lpEntryID->cb, lpEntryID->lpb, szPath, wzPath, fPublicExchangeStore);
  if (lpdwSigHash) *lpdwSigHash = dwSigHash;
  if (lpdwEIDHash) *lpdwEIDHash = dwEIDHash;
  MAPIFreeBuffer(lpMappingSig);
  MAPIFreeBuffer(lpPathPropA);
  MAPIFreeBuffer(lpPathPropW);
  MAPIFreeBuffer(lpConfigProp);
  if (lpProfSect) lpProfSect->Release();
} // ComputeStoreHash
```

> [!TIP]
> <span data-ttu-id="44614-118">Die Funktion HrEmsmdbUIDFromStore funktioniert, ohne im Speicher, versehentlich zu öffnen, sodass es eine gute allgemeine Vorgehensweise ist.</span><span class="sxs-lookup"><span data-stu-id="44614-118">The HrEmsmdbUIDFromStore function works without actually opening the store, so it is a good general purpose approach.</span></span> <span data-ttu-id="44614-119">Jedoch wenn Sie bereits einen Zeiger auf das Store-Objekt ist, können Sie auch Abschnitts Profile GUID direkt aus dem Nachrichtenspeicher abrufen, lesen die PR_EMSMDB_SECTION_UID-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="44614-119">However, if you have a pointer to the store object already, you can also retrieve the profile section GUID directly from the message store by reading the PR_EMSMDB_SECTION_UID property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="44614-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44614-120">See also</span></span>

- [<span data-ttu-id="44614-121">Informationen über die Benachrichtigung-basierten Speicher Indizierung</span><span class="sxs-lookup"><span data-stu-id="44614-121">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
- [<span data-ttu-id="44614-122">Informationen zu MAPI-URLs für die Benachrichtigung-basierte Indizierung</span><span class="sxs-lookup"><span data-stu-id="44614-122">About MAPI URLs for Notification-Based Indexing</span></span>](about-mapi-urls-for-notification-based-indexing.md)

