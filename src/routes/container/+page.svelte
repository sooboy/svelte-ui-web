<script>
    import { Container, Center, Grid } from "@svelteuidev/core";
    import { Badge, Button, Card, Group, Image, Text } from "@svelteuidev/core";
    import { Divider, Menu } from '@svelteuidev/core';
	import { Camera, ChatBubble, Gear, MagnifyingGlass, Trash, Width } from 'radix-icons-svelte';

    const sizes = {
        xs: 540,
        sm: 720,
        md: 960,
        lg: 1140,
        xl: 1320,
    };
</script>

<Container {sizes} size="lg" override={{ bc: "AliceBlue" }}>
    Default container
</Container>

<Container size="xs" override={{ px: "xs", bc: "AliceBlue" }}>
    xs container with xs horizontal padding
</Container>

<Container size={200} override={{ px: 0, bc: "red" }}>
    200px container with 0px horizontal padding
</Container>

<Center>All elements inside Center are centered</Center>

<Grid>
    <Grid.Col span={4}>
        <p>112312</p>
    </Grid.Col>
    <Grid.Col span={4}>2</Grid.Col>
    <Grid.Col span={4}>3</Grid.Col>
</Grid>
<Grid>
    <Grid.Col md={6} lg={3}>1</Grid.Col>
    <Grid.Col md={6} lg={3}>2</Grid.Col>
    <Grid.Col md={6} lg={3}>3</Grid.Col>
    <Grid.Col md={6} lg={3}>
        <Card shadow="lg" padding="lg">
            <Card.Section padding="lg">
                <Image
                    src="https://images.unsplash.com/photo-1555881400-74d7acaacd8b?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=3540&q=80"
                    height={160}
                    alt="Portugal"
                />
            </Card.Section>

            <Group>
                <Text weight={500}>Portugal Porto Adventures</Text>
                <Badge color="pink" variant="light">On Sale</Badge>
            </Group>

            <Text size="sm">
                With Portugal Porto Adventures you can explore more of the
                beautiful portuguese cities, by walking on food, meeting the
                locals and eat excellent food and wine
            </Text>

            <Button variant="light" color="blue" fullSize>
                Book classic tour now
            </Button>
        </Card>
    </Grid.Col>
</Grid>

<Grid cols={24}>
    <Grid.Col xs={24} md={24} span={12}>1</Grid.Col>
    <Grid.Col xs={24} md={24} span={6}>2</Grid.Col>
    <Grid.Col xs={24} md={24} span={4} offset={2} >
        <Menu>
            <Menu.Label>Application</Menu.Label>
            <Menu.Item icon={Gear}>Settings</Menu.Item>
            <Menu.Item icon={ChatBubble}>Messages</Menu.Item>
            <Menu.Item icon={Camera}>Gallery</Menu.Item>
            <Menu.Item icon={MagnifyingGlass}>
                <svelte:fragment slot='rightSection'>
                    <Text size="xs" color="dimmed">⌘K</Text>
                </svelte:fragment>
                Search
            </Menu.Item>
        
            <Divider />
        
            <Menu.Label>Danger zone</Menu.Label>
            <Menu.Item icon={Width}>Transfer my data</Menu.Item>
            <Menu.Item color="red" icon={Trash}>Delete my account</Menu.Item>
        </Menu>
    </Grid.Col>
</Grid>
