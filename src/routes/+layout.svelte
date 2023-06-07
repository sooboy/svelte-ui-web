<script>
    import { SvelteUIProvider } from '@svelteuidev/core';
    import { fns, AppShell, Navbar, Header, Title, Divider } from '@svelteuidev/core';
  </script>
  
  <SvelteUIProvider>
    <AppShell>
        <slot>This is the main content</slot>
    </AppShell>
  </SvelteUIProvider>