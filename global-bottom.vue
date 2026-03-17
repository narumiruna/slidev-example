<template>
  <div v-if="!$nav.isOverview && !$nav.isPresenter" class="deck-footer">
    <span class="deck-page">{{ $nav.currentPage }} / {{ $nav.total }}</span>
    <span class="deck-shortcuts">快捷鍵：←/→ 切頁　F 全螢幕　O 總覽　? 說明</span>
  </div>
</template>

<style scoped>
.deck-footer {
  position: fixed;
  left: 20px;
  right: 20px;
  bottom: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 12px;
  padding: 8px 12px;
  border-radius: 10px;
  background: rgba(32, 22, 15, 0.72);
  color: #fff4e8;
  font-size: 12px;
  line-height: 1;
  letter-spacing: 0.01em;
  pointer-events: none;
  z-index: 60;
}

.deck-page {
  font-weight: 700;
  white-space: nowrap;
}

.deck-shortcuts {
  opacity: 0.92;
  white-space: nowrap;
}

@media (max-width: 900px) {
  .deck-footer {
    left: 10px;
    right: 10px;
    bottom: 8px;
    padding: 7px 10px;
    font-size: 11px;
  }

  .deck-shortcuts {
    display: none;
  }
}
</style>
